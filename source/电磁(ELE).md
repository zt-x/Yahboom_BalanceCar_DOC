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
## 电磁(ELE) 

*TODO*

### 方法

#### ele_Init(void)
电磁传感器采样初始化
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### Get_Adc_ele(u8 ch)
AD采样
<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>ch</td><td>u8</td><td>ADC通道</td></tr>
</table>
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>AD转换结果</td><td>u16</td></tr>
</table>

#### getEleData(void)
获取传感器数据
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### guiyi_way(void)
得到的数据做归一算法
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>当前在磁场的位置</td><td>int</td></tr>
</table>

#### deal_getdata(int a)
处理获取的数据
<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>a</td><td>int</td><td>要处理的数值</td></tr>
</table>
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>处理后的数值</td><td>int</td></tr>
</table>

#### EleDataDeal(void)
数据显示在屏幕上
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

<table border="1">
<tr><th>宏定义</th><th>值</th><th>注释</th></tr>
<tr><td>ELE_L1_Clk</td><td>RCC_APB2Periph_GPIOC</td><td>左侧传感器1的时钟</td></tr>
<tr><td>ELE_L1_Pin</td><td>GPIO_Pin_0</td><td>左侧传感器1的GPIO引脚</td></tr>
<tr><td>ELE_L1_Port</td><td>GPIOC</td><td>左侧传感器1的GPIO端口</td></tr>
<tr><td>ELE_L2_Clk</td><td>RCC_APB2Periph_GPIOC</td><td>左侧传感器2的时钟</td></tr>
<tr><td>ELE_L2_Pin</td><td>GPIO_Pin_1</td><td>左侧传感器2的GPIO引脚</td></tr>
<tr><td>ELE_L2_Port</td><td>GPIOC</td><td>左侧传感器2的GPIO端口</td></tr>
<tr><td>ELE_L3_Clk</td><td>RCC_APB2Periph_GPIOC</td><td>左侧传感器3的时钟</td></tr>
<tr><td>ELE_L3_Pin</td><td>GPIO_Pin_2</td><td>左侧传感器3的GPIO引脚</td></tr>
<tr><td>ELE_L3_Port</td><td>GPIOC</td><td>左侧传感器3的GPIO端口</td></tr>
<tr><td>ELE_MID_Clk</td><td>RCC_APB2Periph_GPIOC</td><td>中间传感器的时钟</td></tr>
<tr><td>ELE_MID_Pin</td><td>GPIO_Pin_3</td><td>中间传感器的GPIO引脚</td></tr>
<tr><td>ELE_MID_Port</td><td>GPIOC</td><td>中间传感器的GPIO端口</td></tr>
<tr><td>ELE_R1_Clk</td><td>RCC_APB2Periph_GPIOC</td><td>右侧传感器1的时钟</td></tr>
<tr><td>ELE_R1_Pin</td><td>GPIO_Pin_4</td><td>右侧传感器1的GPIO引脚</td></tr>
<tr><td>ELE_R1_Port</td><td>GPIOC</td><td>右侧传感器1的GPIO端口</td></tr>
<tr><td>ELE_R2_Clk</td><td>RCC_APB2Periph_GPIOC</td><td>右侧传感器2的时钟</td></tr>
<tr><td>ELE_R2_Pin</td><td>GPIO_Pin_5</td><td>右侧传感器2的GPIO引脚</td></tr>
<tr><td>ELE_R2_Port</td><td>GPIOC</td><td>右侧传感器2的GPIO端口</td></tr>
<tr><td>ELE_R3_Clk</td><td>RCC_APB2Periph_GPIOB</td><td>右侧传感器3的时钟</td></tr>
<tr><td>ELE_R3_Pin</td><td>GPIO_Pin_0</td><td>右侧传感器3的GPIO引脚</td></tr>
<tr><td>ELE_R3_Port</td><td>GPIOB</td><td>右侧传感器3的GPIO端口</td></tr>
<tr><td>ELE_ADC</td><td>ADC2</td><td>使用的ADC</td></tr>
<tr><td>ELE_ADC_CLK</td><td>RCC_APB2Periph_ADC2</td><td>ADC时钟</td></tr>
<tr><td>ELE_L1_CH</td><td>ADC_Channel_10</td><td>左侧传感器1的ADC通道</td></tr>
<tr><td>ELE_L2_CH</td><td>ADC_Channel_11</td><td>左侧传感器2的ADC通道</td></tr>
<tr><td>ELE_L3_CH</td><td>ADC_Channel_12</td><td>左侧传感器3的ADC通道</td></tr>
<tr><td>ELE_M1_CH</td><td>ADC_Channel_13</td><td>中间传感器的ADC通道</td></tr>
<tr><td>ELE_R1_CH</td><td>ADC_Channel_14</td><td>右侧传感器1的ADC通道</td></tr>
<tr><td>ELE_R2_CH</td><td>ADC_Channel_15</td><td>右侧传感器2的ADC通道</td></tr>
<tr><td>ELE_R3_CH</td><td>ADC_Channel_8</td><td>右侧传感器3的ADC通道</td></tr>
</table>

<table border="1">
<tr><th>全局变量</th><th>类型</th><th>注释</th></tr>
<tr><td>ele_seat</td><td>int</td><td>引出算法处理后的变量</td></tr>
<tr><td>Sensor_Left_1</td><td>int</td><td>左侧传感器1的值</td></tr>
<tr><td>Sensor_Left_2</td><td>int</td><td>左侧传感器2的值</td></tr>
<tr><td>Sensor_Left_3</td><td>int</td><td>左侧传感器3的值</td></tr>
<tr><td>Sensor_Right_1</td><td>int</td><td>右侧传感器1的值</td></tr>
<tr><td>Sensor_Right_2</td><td>int</td><td>右侧传感器2的值</td></tr>
<tr><td>Sensor_Right_3</td><td>int</td><td>右侧传感器3的值</td></tr>
<tr><td>Sensor_Middle</td><td>int</td><td>中间传感器的值</td></tr>
</table>
