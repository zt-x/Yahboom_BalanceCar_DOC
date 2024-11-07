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
## 定时器(Timer) *TODO*

### 全局变量
<table border="1">
<tr><th>全局变量</th><th>类型</th><th>注释</th></tr>
<tr><td>battery_All</td><td>float</td><td>累计电池电量</td></tr>
<tr><td>battery_count</td><td>uint8_t</td><td>电池计数</td></tr>
<tr><td>battery_flag</td><td>uint8_t</td><td>电池状态标志</td></tr>
<tr><td>stop_time</td><td>u16</td><td>延迟时间</td></tr>
<tr><td>led_flag</td><td>u16</td><td>指示是否进入闪烁状态</td></tr>
<tr><td>led_twinkle_count</td><td>u16</td><td>LED闪烁计数</td></tr>
<tr><td>led_count</td><td>u16</td><td>LED计数</td></tr>
<tr><td>lower_power_flag</td><td>u8</td><td>低电压标志</td></tr>
<tr><td>bulettohflag</td><td>u8</td><td>指示是否进行蓝牙数据发送</td></tr>
</table>

### 宏定义
<table border="1">
<tr><th>宏定义</th><th>值</th><th>注释</th></tr>
<tr><td>RCC_APB1Periph_TIM6</td><td>(适用平台定时器时钟)</td><td>定时器6时钟</td></tr>
</table>


### 方法

#### TIM6_Init(void)
初始化TIM6，设置定时10毫秒
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### TIM7_Init(void)
初始化TIM7
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### delay_time(u16 time)
延迟指定的时间
<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>time</td><td>u16</td><td>延迟时间，单位：10ms</td></tr>
</table>
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### my_delay(u16 s)
延迟指定的秒数
<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>s</td><td>u16</td><td>要延迟的时间，单位：秒</td></tr>
</table>
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### power_decect(void)
电压处理
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### cotrol_led(void)
控制LED灯状态
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

