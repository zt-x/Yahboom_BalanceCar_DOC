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
    table {font-size:12px;color:#2980b9;width:70%;border-width: 1px;border-color:#2980b9;border-collapse: collapse;margin-bottom: 20px;}
    th {font-size:12px;background-color:#efefef;border-width: 1px;padding: 8px;border-style: solid;border-color: #2980b9;text-align:left;}
    tr {background-color:##efefef;}
    td {font-size:12px;border-width: 1px;padding: 8px;border-style: solid;border-color: #2980b9;}
</style>
## 串口 (Usart)
### 方法
#### uart_init(u32 bound)
初始化串口USART1

<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>bound</td><td>u32</td><td>波特率 (常用: 9600/115200)</td></tr>
</table>

#### USART1_IRQHandler()
USART1中断处理函数

<div class="notice">
    <h2>注意！</h2>
    <p>我们重写了printf()方法用于串口调试输出, 该方法相较于后面的发送函数更加方便</p>
    <p>请优先使用printf()作为输出函数</p>
</div>

#### USART1_Send_U8(uint8_t ch)

发送字符
<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>ch</td><td>uint8_t</td><td>发送的字符</td></tr>
</table>


#### USART1_Send_ArrayU8(uint8_t *BufferPtr, uint16_t Length)

<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>BufferPtr</td><td>uint8_t</td><td>字符串指针</td></tr>
<tr><td>Length</td><td>uint16_t</td><td>字符串长度</td></tr>
</table>




