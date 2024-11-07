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
    table {font-size:12px;color:#2980b9;max-width:80%;min-width:30%;border-width: 1px;border-color:#2980b9;border-collapse: collapse;margin-bottom: 20px;}
    th {font-size:12px;background-color:#efefef;border-width: 1px;padding: 8px;border-style: solid;border-color: #2980b9;text-align:left;}
    tr {background-color:;}
    td {font-size:12px;border-width: 1px;padding: 8px;border-style: solid;border-color: #2980b9;}

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

</style>
## 电池电压(Battery)

### 方法
#### Battery_init()
初始化电池电压测量库

#### Get_Battery_Volotage(void)
*注：Yahboom STM32平衡小车配的电源电压输出范围大致在 8.5~12.5v之间*

获得实际电池分压前电压<br>
实际测量的值比计算得出的值低一点点<br>
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>原始电压值</td><td>float</td></tr>
</table>

#### Battery_Get(uint8_t ch)
获取ADC测量值<br>
<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>ch</td><td>uint8_t</td><td>ADC通道</td></tr>
</table>

<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>获取到的ADC值</td><td>uint16_t</td></tr>
</table>

#### Battery_Get_Average(uint8_t ch, uint8_t times)
获得 ADC 多次测量平均值 <br>
<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>ch</td><td>uint8_t</td><td>ADC通道</td></tr>
<tr><td>times</td><td>uint8_t</td><td>测量次数</td></tr>
</table>

<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>获取到的ADC值</td><td>uint16_t</td></tr>
</table>

#### Get_Measure_Volotage(void)
获得测得原始电压值<br><br>
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>原始电压值</td><td>float</td></tr>
</table>

### 使用示例

<div class="code-container">
<pre><code>
<span class="include">#include</span> <span class="header">&lt;bsp_battery.h&gt;</span>
<span class="keyword">int</span> <span class="function">main</span>()
{
    <span class="function">Battery_init</span>();
    <span class="keyword">while</span>(<span class="number">1</span>){
        // <span class="comment">获取当前电源电压</span>
        <span class="keyword">float</span> v = <span class="function">Get_Battery_Volotage</span>();
    }
}
</code></pre>
</div>
