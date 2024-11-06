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
## 延时(Delay)

void delay_init(void);
void delay_ms(uint16_t nms);
void delay_us(uint32_t nus);

### 方法
#### delay_init(void)
初始化延时函数<br>

#### delay_ms(uint16_t n)

延迟n毫秒<br>
<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>n</td><td>uint16_t</td><td>延迟的时间(毫秒)</td></tr>
</table>

#### delay_us(uint32_t n)

延迟n微秒<br>
<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>n</td><td>uint16_t</td><td>延迟的时间(微秒)</td></tr>
</table>


