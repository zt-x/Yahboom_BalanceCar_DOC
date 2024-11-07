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
## 蜂鸣器(Beep)

### 全局变量

<table border="1">
<tr><th>全局变量</th><th>类型</th><th>注释</th></tr>
<tr><td>beep_time</td><td>u32</td><td>记录蜂鸣器打开时长（单位：ms）</td></tr>
</table>


### 宏定义

<table border="1">
<tr><th>宏定义</th><th>值</th><th>注释</th></tr>
<tr><td>BEEP_RCC</td><td>RCC_APB2Periph_GPIOA</td><td>蜂鸣器的GPIO时钟</td></tr>
<tr><td>BEEP_PORT</td><td>GPIOA</td><td>蜂鸣器控制的GPIO端口</td></tr>
<tr><td>BEEP_PIN</td><td>GPIO_Pin_11</td><td>蜂鸣器控制的GPIO引脚</td></tr>
<tr><td>BEEP_ON</td><td>GPIO_SetBits(BEEP_PORT,BEEP_PIN)</td><td>打开蜂鸣器</td></tr>
<tr><td>BEEP_OFF</td><td>GPIO_ResetBits(BEEP_PORT,BEEP_PIN)</td><td>关闭蜂鸣器</td></tr>
<tr><td>BEEP_BEEP</td><td>PAout(11)</td><td>控制蜂鸣器的输出</td></tr>
</table>

### 方法

#### init_beep(void)
初始化蜂鸣器的引脚
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### open_beep(u32 beep_time)
打开蜂鸣器指定时长
<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>beep_time</td><td>u32</td><td>打开蜂鸣器的时长（单位：ms）</td></tr>
</table>
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>


