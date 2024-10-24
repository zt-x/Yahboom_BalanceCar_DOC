## 串口 (Usart)
**标*号的方法为不常用方法**
### 方法
#### uart_init(u32 bound)

| 参数  | 类型 | 注释   |<br>
| bound | u32  | 波特率 |<br>

初始化串口USART1

#### USART1_Send_U8(uint8_t ch)

| 参数  | 类型     | 注释   |<br>
| ch    | uint8_t  | 发送的字符 |<br>

发送字符

#### USART1_Send_ArrayU8(uint8_t *BufferPtr, uint16_t Length)

| 参数  | 类型     | 注释   |<br>
| BufferPtr | uint8_t  | 字符串指针 |<br>
| Length | uint16_t  | 字符串长度 |<br>


#### USART1_IRQHandler()
USART1中断处理函数



