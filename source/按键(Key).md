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
        max-width: 600px;
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
## 按键(Key) *TODO*

### 方法

#### Key_Scan(GPIO_TypeDef *GPIOx, uint16_t GPIO_Pin)
扫描按键状态
<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>GPIOx</td><td>GPIO_TypeDef*</td><td>GPIO端口</td></tr>
<tr><td>GPIO_Pin</td><td>uint16_t</td><td>GPIO引脚</td></tr>
</table>
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>按键状态</td><td>uint8_t</td></tr>
</table>

#### Key1_GPIO_Init(void)
初始化按键1的GPIO
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### KEYAll_GPIO_Init(void)
初始化所有按键的GPIO
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### Key1_State(uint8_t mode)
读取按键K1的状态
<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>mode</td><td>uint8_t</td><td>设置模式，0：持续按下返回1，1：按下只返回一次1</td></tr>
</table>
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>按键状态</td><td>uint8_t</td></tr>
</table>

#### Key1_Long_Press(uint16_t timeout)
读取按键K1的长按状态
<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>timeout</td><td>uint16_t</td><td>长按时间，单位为秒</td></tr>
</table>
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>1：已达到长按状态，0：未达到</td><td>uint8_t</td></tr>
</table>

#### Key1_is_Press(void)
判断按键是否被按下
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>KEY_PRESS：按下，KEY_RELEASE：松开</td><td>uint8_t</td></tr>
</table>

<table border="1">
<tr><th>宏定义</th><th>值</th><th>注释</th></tr>
<tr><td>KEY1_GPIO_PORT</td><td>GPIOA</td><td>按键1的GPIO端口</td></tr>
<tr><td>KEY1_GPIO_PIN</td><td>GPIO_Pin_8</td><td>按键1的GPIO引脚</td></tr>
<tr><td>KEY1_GPIO_CLK</td><td>RCC_APB2Periph_GPIOA</td><td>按键1的GPIO时钟</td></tr>
<tr><td>KEY_PRESS</td><td>1</td><td>按键被按下</td></tr>
<tr><td>KEY_RELEASE</td><td>0</td><td>按键被松开</td></tr>
<tr><td>KEY_MODE_ONE_TIME</td><td>1</td><td>按下一次返回1</td></tr>
<tr><td>KEY_MODE_ALWAYS</td><td>0</td><td>持续按下返回1</td></tr>
</table>

<table border="1">
<tr><th>全局变量</th><th>类型</th><th>注释</th></tr>
<tr><td>g_key1_long_press</td><td>uint16_t</td><td>记录按键1的长按计时</td></tr>
</table>

