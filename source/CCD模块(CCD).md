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
## CCD模块(CCD) *TODO*

### 全局变量
<table border="1">
<tr><th>全局变量</th><th>类型</th><th>注释</th></tr>
<tr><td>buf_CCD</td><td>char[20]</td><td>用于存储CCD数据显示</td></tr>
<tr><td>ADV</td><td>u16[128]</td><td>存储128个像素的电压值</td></tr>
<tr><td>CCD_Zhongzhi</td><td>u8</td><td>CCD中值</td></tr>
<tr><td>CCD_Yuzhi</td><td>u8</td><td>注释阈值</td></tr>
<tr><td>ADC_128X32</td><td>uint8_t[128]</td><td>返回128个像素点的ADV采集电压值的数组</td></tr>
</table>

### 宏定义
<table border="1">
<tr><th>宏定义</th><th>值</th><th>注释</th></tr>
<tr><td>TSL_SI</td><td>PBout(5)</td><td>SI信号</td></tr>
<tr><td>TSL_CLK</td><td>PBout(4)</td><td>CLK信号</td></tr>
<tr><td>CCD_SI_CLK</td><td>RCC_APB2Periph_GPIOB</td><td>SI信号引脚的时钟</td></tr>
<tr><td>CCD_SI_PIN</td><td>GPIO_Pin_5</td><td>SI信号的GPIO引脚</td></tr>
<tr><td>CCD_SI_PORT</td><td>GPIOB</td><td>SI信号的GPIO端口</td></tr>
<tr><td>CCD_CLK_CLK</td><td>RCC_APB2Periph_GPIOB</td><td>CLK信号引脚的时钟</td></tr>
<tr><td>CCD_CLK_PIN</td><td>GPIO_Pin_4</td><td>CLK信号的GPIO引脚</td></tr>
<tr><td>CCD_CLK_PORT</td><td>GPIOB</td><td>CLK信号的GPIO端口</td></tr>
<tr><td>CCD_AO_CLK</td><td>RCC_APB2Periph_GPIOA</td><td>AO信号引脚的时钟</td></tr>
<tr><td>CCD_AO_PIN</td><td>GPIO_Pin_4</td><td>AO信号的GPIO引脚</td></tr>
<tr><td>CCD_AO_PORT</td><td>GPIOA</td><td>AO信号的GPIO端口</td></tr>
<tr><td>CCD_ADC</td><td>ADC2</td><td>使用的ADC</td></tr>
<tr><td>CCD_ADC_CLK</td><td>RCC_APB2Periph_ADC2</td><td>ADC时钟</td></tr>
<tr><td>CCD_ADC_CH</td><td>ADC_Channel_4</td><td>ADC通道</td></tr>
</table>


### 方法

#### ccd_Init(void)
线性 CCD 初始化
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### Get_Adc_CCD(u8 ch)
AD采样
<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>ch</td><td>u8</td><td>ADC通道</td></tr>
</table>
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>AD转换结果</td><td>u16</td></tr>
</table>



#### Dly_us(void)
延时函数
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### RD_TSL(void)
CCD数据采集
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### deal_data_ccd(void)
开始 CCD 采集并处理输出数据
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### Find_CCD_Zhongzhi(void)
线性 CCD 取中值
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### CCD_Get_ADC_128X32(void)
返回128个像素点的ADV采集电压值，并将幅值压缩成128\*32
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>uint8_t*</td><td>指向存储的128个像素的指针</td></tr>
</table>

#### OLED_Show_CCD_Image(uint8_t* p_img)
在OLED上显示CCD图像
<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>p_img</td><td>uint8_t*</td><td>指向图像数据的指针</td></tr>
</table>
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### binToHex_low(u8 num)
将二进制数转换为低位十六进制
<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>num</td><td>u8</td><td>要转换的数</td></tr>
</table>
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>低位十六进制数</td><td>char</td></tr>
</table>

#### binToHex_high(u8 num)
将二进制数转换为高位十六进制
<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>num</td><td>u8</td><td>要转换的数</td></tr>
</table>
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>高位十六进制数</td><td>char</td></tr>
</table>

#### slove_data(void)
处理获取的数据
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### sendToPc(void)
向PC发送数据
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

