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
## OLED(OLED)

<div class="notice">
    <p>驱动库使用通用性更好的软件（模拟）IIC的方式驱动OLED，但是亚博智能STM32平衡小车V2在硬件电路上是支持硬件IIC的</p>
    <p>本章节内容仅介绍OLED相关方法，不介绍软件IIC的实现</p>
</div>

### 方法
#### void OLED_I2C_Init()

初始化OLED模块

#### void OLED_Clear()

清空屏幕

#### void OLED_Refresh()

刷新屏幕

#### void OLED_Draw_Stringg(char *str, uint8_t x, uint8_t y, bool clear, bool refresh)

在指定位置写入字符串

<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>str</td><td>char *</td><td>想要OLED显示的字符串</td></tr>
<tr><td>x</td><td>uint8_t</td><td>绘制字符串x方向上的起始坐标</td></tr>
<tr><td>y</td><td>uint8_t</td><td>绘制字符串y方向上的起始坐标</td></tr>
<tr><td>clear</td><td>bool</td><td>是否清空屏幕</td></tr>
<tr><td>refresh</td><td>uint8_t</td><td>是否立即屏幕</td></tr>
<tr><td colspan="3">绘制完成后需要调用刷新方法才能显示</td></tr>
</table>


#### void OLED_Draw_Line(char *str, uint8_t line, bool clear, bool refresh)

在指定行写入字符串
/* 写入一行字符 */

<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>str</td><td>char *</td><td>想要OLED显示的字符串</td></tr>
<tr><td>line</td><td>uint8_t</td><td>在第几行显示字符串</td></tr>
<tr><td>clear</td><td>bool</td><td>是否清空屏幕</td></tr>
<tr><td>refresh</td><td>uint8_t</td><td>是否立即屏幕</td></tr>
<tr><td colspan="3">默认行高为10</td></tr>
</table>



