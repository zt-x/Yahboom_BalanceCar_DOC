<style type="text/css">
table {font-size:12px;color:#2980b9;width:50%;border-width: 1px;border-color:#2980b9;border-collapse: collapse;}
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
<tr><td>bound</td><td>u32</td><td>波特率</td></tr>
</table>




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

#### USART1_IRQHandler()
USART1中断处理函数



