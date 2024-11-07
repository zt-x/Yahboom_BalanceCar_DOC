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
## LED(Led) *TODO*

### 宏定义
<table border="1">
<tr><th>宏定义</th><th>值</th><th>注释</th></tr>
<tr><td>LED_RCC</td><td>RCC_APB2Periph_GPIOB</td><td>LED引脚的时钟</td></tr>
<tr><td>LED_PORT</td><td>GPIOB</td><td>LED控制的GPIO端口</td></tr>
<tr><td>LED_PIN</td><td>GPIO_Pin_3</td><td>LED控制的GPIO引脚</td></tr>
<tr><td>LED_ON</td><td>GPIO_SetBits(LED_PORT, LED_PIN)</td><td>打开LED</td></tr>
<tr><td>LED_OFF</td><td>GPIO_ResetBits(LED_PORT, LED_PIN)</td><td>关闭LED</td></tr>
<tr><td>LED</td><td>PBout(3)</td><td>LED的状态控制</td></tr>
</table>

### 方法

#### init_led_gpio(void)
初始化LED的GPIO引脚
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### init_gpio(void)
初始化GPIO引脚
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>