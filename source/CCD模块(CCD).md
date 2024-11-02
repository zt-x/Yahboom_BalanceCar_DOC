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
## CCD模块(CCD)

### 方法
#### Battery_init()
初始化电池电压测量库

#### Get_Battery_Volotage(void)
*注：Yahboom STM32平衡小车配的电源电压输出范围大致在 8.5~12.5v之间*

获得实际电池分压前电压<br>
实际测量的值比计算得出的值低一点点<br>
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>原始电压值</td><td>float</td></tr>
</table>

#### Battery_Get(uint8_t ch)
获取ADC测量值<br>
<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>ch</td><td>uint8_t</td><td>ADC通道</td></tr>
</table>

<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>获取到的ADC值</td><td>uint16_t</td></tr>
</table>

#### Battery_Get_Average(uint8_t ch, uint8_t times)
获得 ADC 多次测量平均值 <br>
<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>ch</td><td>uint8_t</td><td>ADC通道</td></tr>
<tr><td>times</td><td>uint8_t</td><td>测量次数</td></tr>
</table>

<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>获取到的ADC值</td><td>uint16_t</td></tr>
</table>

#### Get_Measure_Volotage(void)
获得测得原始电压值<br><br>
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>原始电压值</td><td>float</td></tr>
</table>


