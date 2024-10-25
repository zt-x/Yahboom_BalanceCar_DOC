## 串口 (Usart)
**标*号的方法为不常用方法**
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

| 参数  | 类型     | 注释   |<br>
| BufferPtr | uint8_t  | 字符串指针 |<br>
| Length | uint16_t  | 字符串长度 |<br>


#### USART1_IRQHandler()
USART1中断处理函数



