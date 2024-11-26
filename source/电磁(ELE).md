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
## 电磁(ELE) 

* *

### 方法

#### ele_Init(void)
电磁传感器采样初始化
<table>
<thead class="table100-head">
<tr><th>返回值</th><th>类型</th></tr>
</thead>
<tbody>
    <tr><td>无</td><td>void</td></tr>
</tbody>
</table>

#### Get_Adc_ele(u8 ch)
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

#### getEleData(void)
获取传感器数据
<table>
<thead class="table100-head">
<tr><th>返回值</th><th>类型</th></tr>
</thead>
<tbody>
    <tr><td>无</td><td>void</td></tr>
</tbody>
</table>

#### guiyi_way(void)
得到的数据做归一算法
<table>
<thead class="table100-head">
<tr><th>返回值</th><th>类型</th></tr>
</thead>
<tbody>
    <tr><td>当前在磁场的位置</td><td>int</td></tr>
</tbody>
</table>

#### deal_getdata(int a)
处理获取的数据
<table>
<thead class="table100-head">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
</thead>
<tbody>
    <tr><td>a</td><td>int</td><td>要处理的数值</td></tr>
</tbody>
</table>
<table>
<thead class="table100-head">
<tr><th>返回值</th><th>类型</th></tr>
</thead>
<tbody>
    <tr><td>处理后的数值</td><td>int</td></tr>
</tbody>
</table>

#### EleDataDeal(void)
数据显示在屏幕上
<table>
<thead class="table100-head">
<tr><th>返回值</th><th>类型</th></tr>
</thead>
<tbody>
    <tr><td>无</td><td>void</td></tr>
</tbody>
</table>

<table>
<thead class="table100-head">
<tr><th>宏定义</th><th>值</th><th>注释</th></tr>
</thead>
<tbody>
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
</tbody>
</table>

<table>
<thead class="table100-head">
<tr><th>全局变量</th><th>类型</th><th>注释</th></tr>
</thead>
<tbody>
    <tr><td>ele_seat</td><td>int</td><td>引出算法处理后的变量</td></tr>
<tr><td>Sensor_Left_1</td><td>int</td><td>左侧传感器1的值</td></tr>
<tr><td>Sensor_Left_2</td><td>int</td><td>左侧传感器2的值</td></tr>
<tr><td>Sensor_Left_3</td><td>int</td><td>左侧传感器3的值</td></tr>
<tr><td>Sensor_Right_1</td><td>int</td><td>右侧传感器1的值</td></tr>
<tr><td>Sensor_Right_2</td><td>int</td><td>右侧传感器2的值</td></tr>
<tr><td>Sensor_Right_3</td><td>int</td><td>右侧传感器3的值</td></tr>
<tr><td>Sensor_Middle</td><td>int</td><td>中间传感器的值</td></tr>
</tbody>
</table>
