## 串口 (Usart)
**标*号的方法为不常用方法**
### 方法
#### uart_init(u32 bound)

| 参数  | 类型 | 注释   |
| ----- | ---- | ------ |
| bound | u32  | 波特率 |

<table id="tfhover" class="tftable" border="1">
<tr><th>Header 1</th><th>Header 2</th><th>Header 3</th><th>Header 4</th><th>Header 5</th></tr>
<tr><td>Row:1 Cell:1</td><td>Row:1 Cell:2</td><td>Row:1 Cell:3</td><td>Row:1 Cell:4</td><td>Row:1 Cell:5</td></tr>
<tr><td>Row:2 Cell:1</td><td>Row:2 Cell:2</td><td>Row:2 Cell:3</td><td>Row:2 Cell:4</td><td>Row:2 Cell:5</td></tr>
<tr><td>Row:3 Cell:1</td><td>Row:3 Cell:2</td><td>Row:3 Cell:3</td><td>Row:3 Cell:4</td><td>Row:3 Cell:5</td></tr>
<tr><td>Row:4 Cell:1</td><td>Row:4 Cell:2</td><td>Row:4 Cell:3</td><td>Row:4 Cell:4</td><td>Row:4 Cell:5</td></tr>
<tr><td>Row:5 Cell:1</td><td>Row:5 Cell:2</td><td>Row:5 Cell:3</td><td>Row:5 Cell:4</td><td>Row:5 Cell:5</td></tr>
<tr><td>Row:6 Cell:1</td><td>Row:6 Cell:2</td><td>Row:6 Cell:3</td><td>Row:6 Cell:4</td><td>Row:6 Cell:5</td></tr>
</table>


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



