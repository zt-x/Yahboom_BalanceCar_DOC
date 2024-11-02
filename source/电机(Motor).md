<style type="text/css">
    body {
        font-family: Arial, sans-serif;
        padding: 20px;
    }

    .notice {
        background-color: #fff3cd; /* 浅黄色背景 */
        color: #856404; /* 深黄色字体 */
        border: 1px solid #ffeeba;
        padding: 15px;
        border-radius: 5px;
        margin: 20px 0 !important;
    }

    table {font-size:12px;color:#2980b9;width:70%;border-width: 1px;border-color:#2980b9;border-collapse: collapse;margin-bottom: 20px;}
    th {font-size:12px;background-color:#efefef;border-width: 1px;padding: 8px;border-style: solid;border-color: #2980b9;text-align:left;}
    tr {background-color:##efefef;}
    td {font-size:12px;border-width: 1px;padding: 8px;border-style: solid;border-color: #2980b9;}
    .code-container {
        background-color: #282c34;
        border-radius: 5px;
        padding: 15px;
        max-width: 600px;
        margin-bottom: 20px;
        overflow-x: auto;
        box-shadow: 0 2px 10px rgba(0, 0, 0, 0.2);
    }
    pre {
        margin: 0;
    }
    code {
        font-family: 'Courier New', Courier, monospace !important;
        white-space: pre-wrap !important; /* Allows code to wrap in case it is too long */
        color: #ffffff !important;
        background-color: #282c34 !important;
        border: none !important;
        font-size: 100% !important;
    }
    .keyword {
        color: #c678dd; /* 紫色 */
        font-weight: bold;
    }
    .function {
        color: #61afef; /* 蓝色 */
    }
    .string {
        color: #98c379; /* 绿色 */
    }
    .include {
        color: #c678dd; /* 紫色 */
    }
    .header {
        color: #98c379; /* 绿色 */
    }
    .number {
        color: #d19a66; /* 橙色 */
    }

    .string {
        color: #56b6c2; /* 青色 */
    }

    .comment {
        color: #7f848e; /* 灰色 */
    }
</style>
## 电机(Motor)

### 宏定义

左电机PWM<br>
<span class="include"> #define L_PWMA   TIM8->CCR1 </span><br>
<span class="include"> #define L_PWMB   TIM8->CCR2 </span><br>
<br>
右电机PWM <br>
<span class="include"> #define R_PWMA   TIM8->CCR3 </span> <br>
<span class="include"> #define R_PWMB   TIM8->CCR4 </span> <br>
</code></pre>

### 方法

#### Balance_PWM_Init(u16 arr,u16 psc)
初始化PWM参数

<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>arr</td><td>u16</td><td>自动重装载值</td></tr>
<tr><td>psc</td><td>u16</td><td>预分频系数</td></tr>
<tr><td colspan="3">通过设定预分频系数和自动重装载值，可以控制PWM的输出频率<br>
平衡小车案例中，默认取值为arr=2880, psc=0</td></tr>
</table>


#### Balance_Motor_Init(void)
使能小车电机连接的GPIO口时钟

#### Set_Pwm(int motor_left,int motor_right)
给小车左右电机发送PWM信号

<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>motor_left</td><td>u16</td><td>左电机的PWM </td></tr>
<tr><td>motor_right</td><td>u16</td><td>右电机的PWM </td></tr>
<tr><td colspan="3">PWM为正数时正转（小车前进方向），为负数时反转（小车后退方向）</td>
</tr>
<tr><td colspan="3">电机有效PWM范围与设定的PWM自动重装载值有关，默认arr=2880时，PWM有效范围为1500~2880</td>
</tr>

</table>

#### 使用示例

<div class="notice">
    <p>1. 务必先执行Balance_Motor_Init(),再执行Balance_PWM_Init()</p>
    <p>2. 驱动电机时,请记得打开小车电源开关</p>
</div>

<div class="code-container">
<pre>
<code>
<span class="include">#include</span> <span class="string">&lt;Motor.h&gt;</span>
<span class="include">#include</span> <span class="string">&lt;delay.h&gt;</span>

<span class="function">Balance_Motor_Init</span>();
<span class="function">Balance_PWM_Init</span>(<span class="number">2880</span>, <span class="number">0</span>);


<span class="keyword">while</span>(<span class="number">1</span>) {
    <span class="function">Set_Pwm</span>(<span class="number">2200</span>, <span class="number">0</span>);
    <span class="function">delay_ms</span>(<span class="number">2000</span>);
    <span class="function">Set_Pwm</span>(<span class="number">0</span>, <span class="number">0</span>);
    <span class="function">delay_ms</span>(<span class="number">2000</span>);
    <span class="function">Set_Pwm</span>(<span class="number">0</span>, <span class="number">2200</span>);
    <span class="function">delay_ms</span>(<span class="number">2000</span>);
    <span class="function">Set_Pwm</span>(<span class="number">0</span>, <span class="number">0</span>);
    <span class="function">delay_ms</span>(<span class="number">2000</span>);
}
</code>
</pre>
</div>
