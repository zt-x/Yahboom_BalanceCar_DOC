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
    /* TABLE TEST */
    .container-table100 {
    width: 100%;
    min-height: 100vh;
    background: #c850c0;
    background: -webkit-linear-gradient(45deg, #4158d0, #c850c0);
    background: -o-linear-gradient(45deg, #4158d0, #c850c0);
    background: -moz-linear-gradient(45deg, #4158d0, #c850c0);
    background: linear-gradient(45deg, #4158d0, #c850c0);

    display: -webkit-box;
    display: -webkit-flex;
    display: -moz-box;
    display: -ms-flexbox;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-wrap: wrap;
    padding: 33px 30px;
    }

    .wrap-table100 {
    width: 1170px;
    }

    table {
    border-spacing: 1;
    border-collapse: collapse;
    background: white;
    border-radius: 10px;
    overflow: hidden;
    width: 100%;
    position: relative;
    }
    table * {
    position: relative;
    }
    table td, table th {
    padding-left: 8px;
    }
    table thead tr {
    height: 60px;
    background: #36304a;
    }
    table tbody tr {
    height: 50px;
    }
    table tbody tr:last-child {
    border: 0;
    }
    table td, table th {
    text-align: left;
    }
    table td.l, table th.l {
    text-align: right;
    }
    table td.c, table th.c {
    text-align: center;
    }
    table td.r, table th.r {
    text-align: center;
    }


    .table100-head th{
    font-family: OpenSans-Regular;
    font-size: 18px;
    color: #fff;
    line-height: 1.2;
    font-weight: unset;
    }

    tbody tr:nth-child(even) {
    background-color: #f5f5f5;
    }

    tbody tr {
    font-family: OpenSans-Regular;
    font-size: 15px;
    color: #808080;
    line-height: 1.2;
    font-weight: unset;
    }

    tbody tr:hover {
    color: #555555;
    background-color: #f5f5f5;
    cursor: pointer;
    }

    .column1 {
    width: 260px;
    padding-left: 40px;
    }

    .column2 {
    width: 160px;
    }

    .column3 {
    width: 245px;
    }

    .column4 {
    width: 110px;
    text-align: right;
    }

    .column5 {
    width: 170px;
    text-align: right;
    }

    .column6 {
    width: 222px;
    text-align: right;
    padding-right: 62px;
    }


    @media screen and (max-width: 992px) {
    table {
        display: block;
    }
    table > *, table tr, table td, table th {
        display: block;
    }
    table thead {
        display: none;
    }
    table tbody tr {
        height: auto;
        padding: 37px 0;
    }
    table tbody tr td {
        padding-left: 40% !important;
        margin-bottom: 24px;
    }
    table tbody tr td:last-child {
        margin-bottom: 0;
    }
    table tbody tr td:before {
        font-family: OpenSans-Regular;
        font-size: 14px;
        color: #999999;
        line-height: 1.2;
        font-weight: unset;
        position: absolute;
        width: 40%;
        left: 30px;
        top: 0;
    }
    table tbody tr td:nth-child(1):before {
        content: "Date";
    }
    table tbody tr td:nth-child(2):before {
        content: "Order ID";
    }
    table tbody tr td:nth-child(3):before {
        content: "Name";
    }
    table tbody tr td:nth-child(4):before {
        content: "Price";
    }
    table tbody tr td:nth-child(5):before {
        content: "Quantity";
    }
    table tbody tr td:nth-child(6):before {
        content: "Total";
    }

    .column4,
    .column5,
    .column6 {
        text-align: left;
    }

    .column4,
    .column5,
    .column6,
    .column1,
    .column2,
    .column3 {
        width: 100%;
    }

    tbody tr {
        font-size: 14px;
    }
    }

    @media (max-width: 576px) {
    .container-table100 {
        padding-left: 15px;
        padding-right: 15px;
    }
    }
    /* TABLE TEST END */

    table {font-size:12px;max-width:80%;min-width:30%;border-width: 0px;border-collapse: collapse;margin-bottom: 20px;box-shadow: rgba(149, 157, 165, 0.2) 0px 8px 24px;}
    th {font-size:12px;border-width: 1px;padding: 8px;text-align:left;}
        td {font-size:12px;border-width: 1px;padding: 8px; vertical-align: middle;font-size: 16px;}
</style>
## CCD模块(CCD) 

* *

### 全局变量
<table>
<thead class="table100-head">
<tr><th>全局变量</th><th>类型</th><th>注释</th></tr>
</thead>
<tbody>
    <tr><td>buf_CCD</td><td>char[20]</td><td>用于存储CCD数据显示</td></tr>
<tr><td>ADV</td><td>u16[128]</td><td>存储128个像素的电压值</td></tr>
<tr><td>CCD_Zhongzhi</td><td>u8</td><td>CCD中值</td></tr>
<tr><td>CCD_Yuzhi</td><td>u8</td><td>注释阈值</td></tr>
<tr><td>ADC_128X32</td><td>uint8_t[128]</td><td>返回128个像素点的ADV采集电压值的数组</td></tr>
</tbody>
</table>

### 宏定义
<table>
<thead class="table100-head">
<tr><th>宏定义</th><th>值</th><th>注释</th></tr>
</thead>
<tbody>
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
</tbody>
</table>


### 方法

#### ccd_Init(void)
线性 CCD 初始化
<table>
<thead class="table100-head">
<tr><th>返回值</th><th>类型</th></tr>
</thead>
<tbody>
    <tr><td>无</td><td>void</td></tr>
</tbody>
</table>

#### Get_Adc_CCD(u8 ch)
AD采样
<table>
<thead class="table100-head">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
</thead>
<tbody>
    <tr><td>ch</td><td>u8</td><td>ADC通道</td></tr>
</tbody>
</table>
<table>
<thead class="table100-head">
<tr><th>返回值</th><th>类型</th></tr>
</thead>
<tbody>
    <tr><td>AD转换结果</td><td>u16</td></tr>
</tbody>
</table>



#### Dly_us(void)
延时函数
<table>
<thead class="table100-head">
<tr><th>返回值</th><th>类型</th></tr>
</thead>
<tbody>
    <tr><td>无</td><td>void</td></tr>
</tbody>
</table>

#### RD_TSL(void)
CCD数据采集
<table>
<thead class="table100-head">
<tr><th>返回值</th><th>类型</th></tr>
</thead>
<tbody>
    <tr><td>无</td><td>void</td></tr>
</tbody>
</table>

#### deal_data_ccd(void)
开始 CCD 采集并处理输出数据
<table>
<thead class="table100-head">
<tr><th>返回值</th><th>类型</th></tr>
</thead>
<tbody>
    <tr><td>无</td><td>void</td></tr>
</tbody>
</table>

#### Find_CCD_Zhongzhi(void)
线性 CCD 取中值
<table>
<thead class="table100-head">
<tr><th>返回值</th><th>类型</th></tr>
</thead>
<tbody>
    <tr><td>无</td><td>void</td></tr>
</tbody>
</table>

#### CCD_Get_ADC_128X32(void)
返回128个像素点的ADV采集电压值，并将幅值压缩成128\*32
<table>
<thead class="table100-head">
<tr><th>返回值</th><th>类型</th></tr>
</thead>
<tbody>
    <tr><td>uint8_t*</td><td>指向存储的128个像素的指针</td></tr>
</tbody>
</table>

#### OLED_Show_CCD_Image(uint8_t* p_img)
在OLED上显示CCD图像
<table>
<thead class="table100-head">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
</thead>
<tbody>
    <tr><td>p_img</td><td>uint8_t*</td><td>指向图像数据的指针</td></tr>
</tbody>
</table>
<table>
<thead class="table100-head">
<tr><th>返回值</th><th>类型</th></tr>
</thead>
<tbody>
    <tr><td>无</td><td>void</td></tr>
</tbody>
</table>

#### binToHex_low(u8 num)
将二进制数转换为低位十六进制
<table>
<thead class="table100-head">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
</thead>
<tbody>
    <tr><td>num</td><td>u8</td><td>要转换的数</td></tr>
</tbody>
</table>
<table>
<thead class="table100-head">
<tr><th>返回值</th><th>类型</th></tr>
</thead>
<tbody>
    <tr><td>低位十六进制数</td><td>char</td></tr>
</tbody>
</table>

#### binToHex_high(u8 num)
将二进制数转换为高位十六进制
<table>
<thead class="table100-head">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
</thead>
<tbody>
    <tr><td>num</td><td>u8</td><td>要转换的数</td></tr>
</tbody>
</table>
<table>
<thead class="table100-head">
<tr><th>返回值</th><th>类型</th></tr>
</thead>
<tbody>
    <tr><td>高位十六进制数</td><td>char</td></tr>
</tbody>
</table>

#### slove_data(void)
处理获取的数据
<table>
<thead class="table100-head">
<tr><th>返回值</th><th>类型</th></tr>
</thead>
<tbody>
    <tr><td>无</td><td>void</td></tr>
</tbody>
</table>

#### sendToPc(void)
向PC发送数据
<table>
<thead class="table100-head">
<tr><th>返回值</th><th>类型</th></tr>
</thead>
<tbody>
    <tr><td>无</td><td>void</td></tr>
</tbody>
</table>

