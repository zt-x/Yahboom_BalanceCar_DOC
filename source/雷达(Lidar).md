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
</style>
## 雷达(Lidar) *TODO*

<div class="notice">
    <p>
        雷达使用STM32上的串口3
    </p>
</div>

### 方法
#### USART3_init(u32 baudrate)
初始化USART3
<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>baudrate</td><td>u32</td><td>波特率</td></tr>
</table>
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### USART3_Send_U8(uint8_t ch)
发送一个字节
<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>ch</td><td>uint8_t</td><td>要发送的字符</td></tr>
</table>
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### USART3_Send_ArrayU8(uint8_t *BufferPtr, uint16_t Length)
发送一个数组
<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>BufferPtr</td><td>uint8_t*</td><td>待发送的数据指针</td></tr>
<tr><td>Length</td><td>uint16_t</td><td>数据长度</td></tr>
</table>
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### USART3_IRQHandler(void)
USART3中断服务函数
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>



