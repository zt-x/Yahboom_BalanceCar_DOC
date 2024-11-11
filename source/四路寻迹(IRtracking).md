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

<table border="1">
<tr><th>宏定义</th><th>值</th><th>注释</th></tr>
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
</table>

#### irtracking_init(void)
初始化红外循迹模块的 GPIO
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>