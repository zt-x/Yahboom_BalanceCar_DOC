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
    td {font-size:12px;border-width: 1px;padding: 8px;}
    .code-container {
        background-color: #282c34;
        border-radius: 5px;
        padding: 15px;
        min-width: 600px;
        margin-bottom: 20px;
        overflow-x: auto;
        box-shadow: 0 2px 10px rgba(0, 0, 0, 0.2);
    }
    pre {
        margin: 0;
    }
    code {
        font-family: 'Courier New', Courier, monospace !important;
        white-space: pre-wrap !important; /* Allows code to wrap in case it is too long */
        color: #ffffff !important;
        background-color: #282c34 !important;
        border: none !important;
        font-size: 100% !important;
    }
    .keyword {
        color: #c678dd; /* 紫色 */
        font-weight: bold;
    }
    .function {
        color: #61afef; /* 蓝色 */
    }
    .string {
        color: #98c379; /* 绿色 */
    }
    .include {
        color: #c678dd; /* 紫色 */
    }
    .header {
        color: #98c379; /* 绿色 */
    }
    .number {
        color: #d19a66; /* 橙色 */
    }

    .string {
        color: #56b6c2; /* 青色 */
    }

    .comment {
        color: #7f848e; /* 灰色 */
    }

</style>
## 四路寻迹(IRtracking) 

<table>
<thead class="table100-head">
<tr><th>宏定义</th><th>值</th><th>注释</th></tr>
</thead>
<tbody>
    <tr><td>IR_X1_Clk</td><td>RCC_APB2Periph_GPIOC</td><td>IR X1模块的GPIO时钟</td></tr>
<tr><td>IR_X1_Pin</td><td>GPIO_Pin_4</td><td>IR X1模块的GPIO引脚</td></tr>
<tr><td>IR_X1_Port</td><td>GPIOC</td><td>IR X1模块的GPIO端口</td></tr>

<tr><td>IR_X2_Clk</td><td>RCC_APB2Periph_GPIOC</td><td>IR X2模块的GPIO时钟</td></tr>
<tr><td>IR_X2_Pin</td><td>GPIO_Pin_5</td><td>IR X2模块的GPIO引脚</td></tr>
<tr><td>IR_X2_Port</td><td>GPIOC</td><td>IR X2模块的GPIO端口</td></tr>

<tr><td>IR_X3_Clk</td><td>RCC_APB2Periph_GPIOB</td><td>IR X3模块的GPIO时钟</td></tr>
<tr><td>IR_X3_Pin</td><td>GPIO_Pin_0</td><td>IR X3模块的GPIO引脚</td></tr>
<tr><td>IR_X3_Port</td><td>GPIOB</td><td>IR X3模块的GPIO端口</td></tr>

<tr><td>IR_X4_Clk</td><td>RCC_APB2Periph_GPIOB</td><td>IR X4模块的GPIO时钟</td></tr>
<tr><td>IR_X4_Pin</td><td>GPIO_Pin_1</td><td>IR X4模块的GPIO引脚</td></tr>
<tr><td>IR_X4_Port</td><td>GPIOB</td><td>IR X4模块的GPIO端口</td></tr>

<div class="notice">
    <p> 初始化成功后，直接使用下述宏定义获取四路循迹状态即可 </p>
</div>

<tr><td>IN_X1</td><td>GPIO_ReadInputDataBit(IR_X1_Port, IR_X1_Pin)</td><td>读取IR X1模块的输入状态</td></tr>
<tr><td>IN_X2</td><td>GPIO_ReadInputDataBit(IR_X2_Port, IR_X2_Pin)</td><td>读取IR X2模块的输入状态</td></tr>
<tr><td>IN_X3</td><td>GPIO_ReadInputDataBit(IR_X3_Port, IR_X3_Pin)</td><td>读取IR X3模块的输入状态</td></tr>
<tr><td>IN_X4</td><td>GPIO_ReadInputDataBit(IR_X4_Port, IR_X4_Pin)</td><td>读取IR X4模块的输入状态</td></tr>
</tbody>
</table>

#### irtracking_init(void)
初始化红外循迹模块的 GPIO
<table>
<thead class="table100-head">
<tr><th>返回值</th><th>类型</th></tr>
</thead>
<tbody>
    <tr><td>无</td><td>void</td></tr>
</tbody>
</table>