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
## PS2(PS2) 
*TODO*

### 全局变量
<table border="1">
<tr><th>全局变量</th><th>类型</th><th>注释</th></tr>
<tr><td>Handkey</td><td>u16</td><td>按键值读取临时存储</td></tr>
<tr><td>Comd</td><td>u8[2]</td><td>开始命令数组</td></tr>
<tr><td>Data</td><td>u8[9]</td><td>数据存储数组</td></tr>
<tr><td>MASK</td><td>u16[16]</td><td>按键掩码数组</td></tr>
</table>

### 宏定义
<table border="1">
<tr><th>宏定义</th><th>值</th><th>注释</th></tr>
<tr><td>PS_RCC_DI</td><td>RCC_APB2Periph_GPIOB</td><td>数据输入DI引脚的时钟</td></tr>
<tr><td>PS_RCC_DO</td><td>RCC_APB2Periph_GPIOB</td><td>数据输出DO引脚的时钟</td></tr>
<tr><td>PS_RCC_CS</td><td>RCC_APB2Periph_GPIOB</td><td>片选CS引脚的时钟</td></tr>
<tr><td>PS_RCC_CLK</td><td>RCC_APB2Periph_GPIOB</td><td>时钟CLK引脚的时钟</td></tr>
<tr><td>PS_PIN_DI</td><td>GPIO_Pin_14</td><td>数据输入DI引脚</td></tr>
<tr><td>PS_PIN_DO</td><td>GPIO_Pin_15</td><td>数据输出DO引脚</td></tr>
<tr><td>PS_PIN_CS</td><td>GPIO_Pin_12</td><td>片选CS引脚</td></tr>
<tr><td>PS_PIN_CLK</td><td>GPIO_Pin_13</td><td>时钟CLK引脚</td></tr>
<tr><td>PS_PORT_DI</td><td>GPIOB</td><td>DI引脚的GPIO端口</td></tr>
<tr><td>PS_PORT_DO</td><td>GPIOB</td><td>DO引脚的GPIO端口</td></tr>
<tr><td>PS_PORT_CS</td><td>GPIOB</td><td>CS引脚的GPIO端口</td></tr>
<tr><td>PS_PORT_CLK</td><td>GPIOB</td><td>CLK引脚的GPIO端口</td></tr>
<tr><td>DI</td><td>PBin(14)</td><td>数据输入</td></tr>
<tr><td>DO_H</td><td>PBout(15)=1</td><td>命令位高</td></tr>
<tr><td>DO_L</td><td>PBout(15)=0</td><td>命令位低</td></tr>
<tr><td>CS_H</td><td>PBout(12)=1</td><td>CS拉高</td></tr>
<tr><td>CS_L</td><td>PBout(12)=0</td><td>CS拉低</td></tr>
<tr><td>CLK_H</td><td>PBout(13)=1</td><td>时钟拉高</td></tr>
<tr><td>CLK_L</td><td>PBout(13)=0</td><td>时钟拉低</td></tr>
<tr><td>PSB_*</td><td>对应的按键值</td><td>各种按键的常量定义</td></tr>
</table>


### 方法

#### PS2_Init(void)
PS2接收器模块初始化
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### PS2_Cmd(u8 CMD)
向手柄发送命令
<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>CMD</td><td>u8</td><td>要发送的命令</td></tr>
</table>
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### PS2_RedLight(void)
判断是否为红灯模式
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>0</td><td>u8</td><td>红灯模式</td></tr>
<tr><td>1</td><td>u8</td><td>其他模式</td></tr>
</table>

#### PS2_ReadData(void)
读取手柄数据
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### PS2_DataKey(void)
读取按键值
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>按键值</td><td>u8</td></tr>
</table>

#### PS2_AnologData(u8 button)
获取摇杆的模拟值
<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>button</td><td>u8</td><td>要读取的摇杆按钮</td></tr>
</table>
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>模拟值</td><td>u8</td></tr>
</table>

#### PS2_ClearData(void)
清除数据缓冲区
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### PS2_Vibration(u8 motor1, u8 motor2)
设置手柄震动
<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>motor1</td><td>u8</td><td>右侧小震动电机（0x00关，其他开）</td></tr>
<tr><td>motor2</td><td>u8</td><td>左侧大震动电机（0x40~0xFF开，值越大震动越大）</td></tr>
</table>
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### PS2_ShortPoll(void)
短轮询
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### PS2_EnterConfing(void)
进入配置模式
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### PS2_TurnOnAnalogMode(void)
发送模拟量模式设置
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### PS2_VibrationMode(void)
设置振动模式
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### PS2_ExitConfing(void)
完成并保存配置
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### PS2_SetInit(void)
控制器配置初始化
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### PS2_Data_Show(void)
按键值测试及输出函数
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>





