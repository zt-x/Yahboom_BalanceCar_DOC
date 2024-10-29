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
            margin: 20px 0;
        }

        .notice h2 {
            margin: 0 0 10px;
        }

        .notice p {
            margin: 0;
        }
    table {font-size:12px;color:#2980b9;width:50%;border-width: 1px;border-color:#2980b9;border-collapse: collapse;margin-bottom: 20px;}
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
    .notice {
        background-color: #fff3cd; /* 浅黄色背景 */
        color: #856404; /* 深黄色字体 */
        border: 1px solid #ffeeba;
        padding: 15px;
        border-radius: 5px;
        margin: 20px 0;
    }
</style>
## 超声波(Ultrasonic)

<div class="notice">
    <p>此模块依赖延迟函数delay_ms, 使用该模块时请导入delay模块</p>
</div>

### 方法
#### ultrasonic_init()
初始化电池电压测量库 <br>
用于初始化超声波传感器接口的，主要使用了STM32微控制器的GPIO（通用输入输出）和定时器功能
#### get_distance(void) 
*返回值单位为毫米 (mm)*
返回超声波传感器测得的距离<br>

<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>距离(mm)</td><td>int</td></tr>
</table>

<div class="code-container">
<pre><code>
<span class="include">#include</span> <span class="header">"&lt;bsp_ultrasonic.h&gt;"</span>
<span class="include">#include</span> <span class="header">"&lt;delay.h&gt;"</span>
<span class="keyword">int</span> <span class="function">main</span>()
{
    // <span class="comment">超声测距模块依赖延时模块</span>
    <span class="function">delay_init</span>();
    <span class="function">ultrasonic_init</span>();

    <span class="keyword">while</span>(<span class="number">1</span>){
        <span class="function">printf</span>(<span class="string">"dis: %dmm\n"</span>, <span class="function">get_distance</span>());
        <span class="function">delay_ms</span>(<span class="number">100</span>);
    }

    <span class="keyword">return</span> <span class="number">0</span>;
}
</code></pre>
</div>




