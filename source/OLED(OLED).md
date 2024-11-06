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

    table {font-size:12px;color:#2980b9;max-width:80%;min-width:30%;border-width: 1px;border-color:#2980b9;border-collapse: collapse;margin-bottom: 20px;}
    th {font-size:12px;background-color:#efefef;border-width: 1px;padding: 8px;border-style: solid;border-color: #2980b9;text-align:left;}
    tr {background-color:;}
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

<div class="notice">
    <p> 下述方法为驱动芯片SSD1306提供，可以进行更细致的绘制操作 </p>
</div>



#### SSD1306_UpdateScreen()
单位更新OLED显示屏内容
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### SSD1306_ToggleInvert()
切换OLED显示的颜色反转
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### SSD1306_Fill(SSD1306_COLOR_t Color)
填充屏幕的颜色
<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>Color</td><td>SSD1306_COLOR_t</td><td>填充颜色</td></tr>
</table>
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### SSD1306_DrawPixel(uint16_t x, uint16_t y, SSD1306_COLOR_t color)
在指定坐标绘制一个像素
<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>x</td><td>uint16_t</td><td>x坐标</td></tr>
<tr><td>y</td><td>uint16_t</td><td>y坐标</td></tr>
<tr><td>color</td><td>SSD1306_COLOR_t</td><td>像素颜色</td></tr>
</table>
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### SSD1306_GotoXY(uint16_t x, uint16_t y)
设置下一个字符的绘制坐标
<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>x</td><td>uint16_t</td><td>x坐标</td></tr>
<tr><td>y</td><td>uint16_t</td><td>y坐标</td></tr>
</table>
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### SSD1306_Putc(char ch, FontDef_t *Font, SSD1306_COLOR_t color)
绘制单个字符
<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>ch</td><td>char</td><td>要绘制的字符</td></tr>
<tr><td>Font</td><td>FontDef_t*</td><td>使用的字体结构体</td></tr>
<tr><td>color</td><td>SSD1306_COLOR_t</td><td>字符颜色</td></tr>
</table>
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>char</td></tr>
</table>

#### SSD1306_Puts(char *str, FontDef_t *Font, SSD1306_COLOR_t color)
绘制字符串
<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>str</td><td>char*</td><td>要绘制的字符串</td></tr>
<tr><td>Font</td><td>FontDef_t*</td><td>使用的字体结构体</td></tr>
<tr><td>color</td><td>SSD1306_COLOR_t</td><td>字符串颜色</td></tr>
</table>
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>char</td></tr>
</table>

#### SSD1306_DrawLine(uint16_t x0, uint16_t y0, uint16_t x1, uint16_t y1, SSD1306_COLOR_t c)
绘制一条线
<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>x0</td><td>uint16_t</td><td>起始点x坐标</td></tr>
<tr><td>y0</td><td>uint16_t</td><td>起始点y坐标</td></tr>
<tr><td>x1</td><td>uint16_t</td><td>结束点x坐标</td></tr>
<tr><td>y1</td><td>uint16_t</td><td>结束点y坐标</td></tr>
<tr><td>c</td><td>SSD1306_COLOR_t</td><td>线条颜色</td></tr>
</table>
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### SSD1306_DrawRectangle(uint16_t x, uint16_t y, uint16_t w, uint16_t h, SSD1306_COLOR_t c)
绘制矩形
<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>x</td><td>uint16_t</td><td>左上角x坐标</td></tr>
<tr><td>y</td><td>uint16_t</td><td>左上角y坐标</td></tr>
<tr><td>w</td><td>uint16_t</td><td>矩形宽度</td></tr>
<tr><td>h</td><td>uint16_t</td><td>矩形高度</td></tr>
<tr><td>c</td><td>SSD1306_COLOR_t</td><td>矩形颜色</td></tr>
</table>
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### SSD1306_DrawFilledRectangle(uint16_t x, uint16_t y, uint16_t w, uint16_t h, SSD1306_COLOR_t c)
绘制填充矩形
<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>x</td><td>uint16_t</td><td>左上角x坐标</td></tr>
<tr><td>y</td><td>uint16_t</td><td>左上角y坐标</td></tr>
<tr><td>w</td><td>uint16_t</td><td>矩形宽度</td></tr>
<tr><td>h</td><td>uint16_t</td><td>矩形高度</td></tr>
<tr><td>c</td><td>SSD1306_COLOR_t</td><td>矩形颜色</td></tr>
</table>
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### SSD1306_DrawTriangle(uint16_t x1, uint16_t y1, uint16_t x2, uint16_t y2, uint16_t x3, uint16_t y3, SSD1306_COLOR_t color)
绘制三角形
<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>x1</td><td>uint16_t</td><td>第一点x坐标</td></tr>
<tr><td>y1</td><td>uint16_t</td><td>第一点y坐标</td></tr>
<tr><td>x2</td><td>uint16_t</td><td>第二点x坐标</td></tr>
<tr><td>y2</td><td>uint16_t</td><td>第二点y坐标</td></tr>
<tr><td>x3</td><td>uint16_t</td><td>第三点x坐标</td></tr>
<tr><td>y3</td><td>uint16_t</td><td>第三点y坐标</td></tr>
<tr><td>color</td><td>SSD1306_COLOR_t</td><td>三角形颜色</td></tr>
</table>
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### SSD1306_DrawCircle(int16_t x0, int16_t y0, int16_t r, SSD1306_COLOR_t c)
绘制圆形
<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>x0</td><td>int16_t</td><td>圆心x坐标</td></tr>
<tr><td>y0</td><td>int16_t</td><td>圆心y坐标</td></tr>
<tr><td>r</td><td>int16_t</td><td>半径</td></tr>
<tr><td>c</td><td>SSD1306_COLOR_t</td><td>圆形颜色</td></tr>
</table>
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### SSD1306_DrawFilledCircle(int16_t x0, int16_t y0, int16_t r, SSD1306_COLOR_t c)
绘制填充圆形
<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>x0</td><td>int16_t</td><td>圆心x坐标</td></tr>
<tr><td>y0</td><td>int16_t</td><td>圆心y坐标</td></tr>
<tr><td>r</td><td>int16_t</td><td>半径</td></tr>
<tr><td>c</td><td>SSD1306_COLOR_t</td><td>填充圆形颜色</td></tr>
</table>
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### ssd1306_I2C_Init()
初始化I2C接口
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### ssd1306_I2C_Write(uint8_t address, uint8_t reg, uint8_t data)
向指定地址和寄存器写入数据
<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>address</td><td>uint8_t</td><td>I2C设备地址</td></tr>
<tr><td>reg</td><td>uint8_t</td><td>寄存器地址</td></tr>
<tr><td>data</td><td>uint8_t</td><td>要写入的数据</td></tr>
</table>
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### ssd1306_I2C_WriteMulti(uint8_t address, uint8_t reg, uint8_t *data, uint16_t count)
向指定地址和寄存器写入多个数据
<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>address</td><td>uint8_t</td><td>I2C设备地址</td></tr>
<tr><td>reg</td><td>uint8_t</td><td>寄存器地址</td></tr>
<tr><td>data</td><td>uint8_t*</td><td>指向数据的指针</td></tr>
<tr><td>count</td><td>uint16_t</td><td>要写入的数据数量</td></tr>
</table>
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

### 使用示例

<div class="code-container">
<pre>
<code>
// <span class="comment"> 导入部分代码省略 </span>
<span class="keyword">int</span> <span class="keyword">main</span>() {
    <span class="function">OLED_I2C_Init</span>();
    <span class="function">OLED_Clear</span>();
    <span class="keyword">while</span>(<span class="number">1</span>) {
        <span class="function">OLED_DrawLine</span>(<span class="string">"Hello Yahboom!"</span>,<span class="number">1</span>, <span class="number">0</span>, true, true);
    }
    <span class="keyword">return</span> <span class="number">0</span>;
}
</code>
</pre>
</div>
