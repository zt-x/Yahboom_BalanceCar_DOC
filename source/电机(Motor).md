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
    .notice h2 {
        margin: 0 0 10px;
    }

    .notice p {
        margin: 0;
    }
    /* TABLE TEST */
    .container-table100 {
    width: 100%;
    min-height: 100vh;
    background: #c850c0;
    background: -webkit-linear-gradient(45deg, #4158d0, #c850c0);
    background: -o-linear-gradient(45deg, #4158d0, #c850c0);
    background: -moz-linear-gradient(45deg, #4158d0, #c850c0);
    background: linear-gradient(45deg, #4158d0, #c850c0);

    display: -webkit-box;
    display: -webkit-flex;
    display: -moz-box;
    display: -ms-flexbox;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-wrap: wrap;
    padding: 33px 30px;
    }

    .wrap-table100 {
    width: 1170px;
    }

    table {
    border-spacing: 1;
    border-collapse: collapse;
    background: white;
    border-radius: 10px;
    overflow: hidden;
    width: 100%;
    position: relative;
    }
    table * {
    position: relative;
    }
    table td, table th {
    padding-left: 8px;
    }
    table thead tr {
    height: 60px;
    background: #36304a;
    }
    table tbody tr {
    height: 50px;
    }
    table tbody tr:last-child {
    border: 0;
    }
    table td, table th {
    text-align: left;
    }
    table td.l, table th.l {
    text-align: right;
    }
    table td.c, table th.c {
    text-align: center;
    }
    table td.r, table th.r {
    text-align: center;
    }


    .table100-head th{
    font-family: OpenSans-Regular;
    font-size: 18px;
    color: #fff;
    line-height: 1.2;
    font-weight: unset;
    }

    tbody tr:nth-child(even) {
    background-color: #f5f5f5;
    }

    tbody tr {
    font-family: OpenSans-Regular;
    font-size: 15px;
    color: #808080;
    line-height: 1.2;
    font-weight: unset;
    }

    tbody tr:hover {
    color: #555555;
    background-color: #f5f5f5;
    cursor: pointer;
    }

    .column1 {
    width: 260px;
    padding-left: 40px;
    }

    .column2 {
    width: 160px;
    }

    .column3 {
    width: 245px;
    }

    .column4 {
    width: 110px;
    text-align: right;
    }

    .column5 {
    width: 170px;
    text-align: right;
    }

    .column6 {
    width: 222px;
    text-align: right;
    padding-right: 62px;
    }


    @media screen and (max-width: 992px) {
    table {
        display: block;
    }
    table > *, table tr, table td, table th {
        display: block;
    }
    table thead {
        display: none;
    }
    table tbody tr {
        height: auto;
        padding: 37px 0;
    }
    table tbody tr td {
        padding-left: 40% !important;
        margin-bottom: 24px;
    }
    table tbody tr td:last-child {
        margin-bottom: 0;
    }
    table tbody tr td:before {
        font-family: OpenSans-Regular;
        font-size: 14px;
        color: #999999;
        line-height: 1.2;
        font-weight: unset;
        position: absolute;
        width: 40%;
        left: 30px;
        top: 0;
    }
    table tbody tr td:nth-child(1):before {
        content: "Date";
    }
    table tbody tr td:nth-child(2):before {
        content: "Order ID";
    }
    table tbody tr td:nth-child(3):before {
        content: "Name";
    }
    table tbody tr td:nth-child(4):before {
        content: "Price";
    }
    table tbody tr td:nth-child(5):before {
        content: "Quantity";
    }
    table tbody tr td:nth-child(6):before {
        content: "Total";
    }

    .column4,
    .column5,
    .column6 {
        text-align: left;
    }

    .column4,
    .column5,
    .column6,
    .column1,
    .column2,
    .column3 {
        width: 100%;
    }

    tbody tr {
        font-size: 14px;
    }
    }

    @media (max-width: 576px) {
    .container-table100 {
        padding-left: 15px;
        padding-right: 15px;
    }
    }
    /* TABLE TEST END */

    table {font-size:12px;max-width:80%;min-width:30%;border-width: 0px;border-collapse: collapse;margin-bottom: 20px;box-shadow: rgba(149, 157, 165, 0.2) 0px 8px 24px;}
    th {font-size:12px;border-width: 1px;padding: 8px;text-align:left;}
    td {font-size:12px;border-width: 1px;padding: 8px;}
    .code-container {
        background-color: #282c34;
        border-radius: 5px;
        padding: 15px;
        min-width: 600px;
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

<table>
<thead class="table100-head">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
</thead>
<tbody>
    <tr><td>arr</td><td>u16</td><td>自动重装载值</td></tr>
<tr><td>psc</td><td>u16</td><td>预分频系数</td></tr>
<tr><td colspan="3">通过设定预分频系数和自动重装载值，可以控制PWM的输出频率<br>
平衡小车案例中，默认取值为arr=2880, psc=0</td></tr>
</tbody>
</table>


#### Balance_Motor_Init(void)
使能小车电机连接的GPIO口时钟

#### Set_Pwm(int motor_left,int motor_right)
给小车左右电机发送PWM信号

<table>
<thead class="table100-head">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
</thead>
<tbody>
    <tr><td>motor_left</td><td>u16</td><td>左电机的PWM </td></tr>
<tr><td>motor_right</td><td>u16</td><td>右电机的PWM </td></tr>
<tr><td colspan="3">PWM为正数时正转（小车前进方向），为负数时反转（小车后退方向）</td>
</tr>
<tr><td colspan="3">电机有效PWM范围与设定的PWM自动重装载值有关，默认arr=2880时，PWM有效范围为1500~2880</td>
</tr>

</table>

### 使用示例

<div class="notice">
    <p>1. 务必先执行Balance_Motor_Init(),再执行Balance_PWM_Init()</p>
    <p>2. 驱动电机时,请记得打开小车电源开关</p>
    <p>3. 如果要使用编码器Encoder, 请确保初始化电机的函数要在初始化编码器定时器的函数<b>之前</b>调用!!</p>
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
