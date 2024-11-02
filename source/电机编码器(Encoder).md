<style type="text/css">
        body {
            font-family: Arial, sans-serif;
            padding: 20px;
        }

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
    .notice {
        background-color: #fff3cd; /* 浅黄色背景 */
        color: #856404; /* 深黄色字体 */
        border: 1px solid #ffeeba;
        padding: 15px;
        border-radius: 5px;
        margin: 20px 0;
    }
    table {font-size:12px;color:#2980b9;width:70%;border-width: 1px;border-color:#2980b9;border-collapse: collapse;margin-bottom: 20px;}
    th {font-size:12px;background-color:#efefef;border-width: 1px;padding: 8px;border-style: solid;border-color: #2980b9;text-align:left;}
    tr {background-color:##efefef;}
    td {font-size:12px;border-width: 1px;padding: 8px;border-style: solid;border-color: #2980b9;}
</style>
## 电机编码器(Encoder)

### 宏定义
定时器的自动重装载值,不可大于65535 因为F103的定时器是16位的。
#define ENCODER_TIM_PERIOD (u16)(65535)

计算转速需要的参数
#define PI 3.14159265							//PI圆周率
#define Control_Frequency  200.0	//编码器读取频率
#define Diameter_67  67.0 				//轮子直径67mm 
#define EncoderMultiples   4.0 		//编码器倍频数
#define Encoder_precision  11.0 	//编码器精度 11线
#define Reduction_Ratio  30.0			//减速比30
#define Perimeter  210.4867 			//周长，单位mm

左右轮的ID
typedef enum {
    MOTOR_ID_ML = 0,
    MOTOR_ID_MR,
    MAX_MOTOR
} Motor_ID;

### 方法

#### Encoder_Init_TIM3(void)
初始化TIM3定时器
<table border="1">
    <tr>
        <th>设置项目</th>
        <th>设置值</th>
    </tr>
    <tr>
        <td>预分频器</td>
        <td>0</td>
    </tr>
    <tr>
        <td>自动重装值</td>
        <td>ENCODER_TIM_PERIOD（具体值需查看代码）</td>
    </tr>
    <tr>
        <td>时钟分频</td>
        <td>不分频 (TIM_CKD_DIV1)</td>
    </tr>
    <tr>
        <td>计数模式</td>
        <td>向上计数 (TIM_CounterMode_Up)</td>
    </tr>
    <tr>
        <td>输入捕获滤波</td>
        <td>10</td>
    </tr>
    <tr>
        <td>GPIO引脚</td>
        <td>GPIO_Pin_6 和 GPIO_Pin_7</td>
    </tr>
    <tr>
        <td>GPIO模式</td>
        <td>浮空输入 (GPIO_Mode_IN_FLOATING)</td>
    </tr>
    <tr>
        <td>定时器3时钟使能</td>
        <td>使能定时器3的时钟</td>
    </tr>
    <tr>
        <td>PA端口时钟使能</td>
        <td>使能PA端口时钟</td>
    </tr>
    <tr>
        <td>编码器模式</td>
        <td>编码器模式3 (TIM_EncoderMode_TI12)</td>
    </tr>
    <tr>
        <td>输入捕获极性</td>
        <td>上升沿触发 (TIM_ICPolarity_Rising)</td>
    </tr>
    <tr>
        <td>TIM更新标志位清除</td>
        <td>清除TIM的更新标志位</td>
    </tr>
    <tr>
        <td>TIM更新中断使能</td>
        <td>使能TIM更新中断</td>
    </tr>
</table>

#### Encoder_Init_TIM4(void)
初始化TIM4定时器
<table border="1">
    <tr>
        <th>设置项目</th>
        <th>设置值</th>
    </tr>
    <tr>
        <td>定时器结构体</td>
        <td>TIM_TimeBaseInitTypeDef TIM_TimeBaseStructure</td>
    </tr>
    <tr>
        <td>输入捕获结构体</td>
        <td>TIM_ICInitTypeDef TIM_ICInitStructure</td>
    </tr>
    <tr>
        <td>GPIO初始化结构体</td>
        <td>GPIO_InitTypeDef GPIO_InitStructure</td>
    </tr>
    <tr>
        <td>定时器4时钟使能</td>
        <td>使能定时器4的时钟 (RCC_APB1PeriphClockCmd(RCC_APB1Periph_TIM4, ENABLE))</td>
    </tr>
    <tr>
        <td>PB端口时钟使能</td>
        <td>使能PB端口时钟 (RCC_APB2PeriphClockCmd(RCC_APB2Periph_GPIOB, ENABLE))</td>
    </tr>
    <tr>
        <td>GPIO引脚配置</td>
        <td>GPIO_Pin_6 | GPIO_Pin_7</td>
    </tr>
    <tr>
        <td>GPIO模式</td>
        <td>浮空输入 (GPIO_Mode_IN_FLOATING)</td>
    </tr>
    <tr>
        <td>GPIO初始化</td>
        <td>根据设定参数初始化GPIOB (GPIO_Init(GPIOB, &GPIO_InitStructure))</td>
    </tr>
    <tr>
        <td>定时器基础配置初始化</td>
        <td>TIM_TimeBaseStructInit(&TIM_TimeBaseStructure)</td>
    </tr>
    <tr>
        <td>预分频器</td>
        <td>0x0</td>
    </tr>
    <tr>
        <td>计数器自动重装值</td>
        <td>ENCODER_TIM_PERIOD</td>
    </tr>
    <tr>
        <td>时钟分频</td>
        <td>不分频 (TIM_CKD_DIV1)</td>
    </tr>
    <tr>
        <td>计数模式</td>
        <td>向上计数 (TIM_CounterMode_Up)</td>
    </tr>
    <tr>
        <td>定时器初始化</td>
        <td>TIM_TimeBaseInit(TIM4, &TIM_TimeBaseStructure)</td>
    </tr>
    <tr>
        <td>编码器接口配置</td>
        <td>使用编码器模式3 (TIM_EncoderInterfaceConfig(TIM4, TIM_EncoderMode_TI12, TIM_ICPolarity_Rising, TIM_ICPolarity_Rising))</td>
    </tr>
    <tr>
        <td>输入捕获结构体初始化</td>
        <td>TIM_ICStructInit(&TIM_ICInitStructure)</td>
    </tr>
    <tr>
        <td>输入捕获滤波</td>
        <td>10</td>
    </tr>
    <tr>
        <td>输入捕获初始化</td>
        <td>TIM_ICInit(TIM4, &TIM_ICInitStructure)</td>
    </tr>
    <tr>
        <td>TIM更新标志位清除</td>
        <td>清除TIM的更新标志位 (TIM_ClearFlag(TIM4, TIM_FLAG_Update))</td>
    </tr>
    <tr>
        <td>TIM更新中断使能</td>
        <td>使能TIM更新中断 (TIM_ITConfig(TIM4, TIM_IT_Update, ENABLE))</td>
    </tr>
</table>


#### Read_Encoder(Motor_ID MYTIMX)
单位时间读取编码器计数

<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>MYTIMX</td><td>Motor_ID</td><td>选择一个电机读取</td></tr>
<tr><td colspan="3"><br>
Motor_ID可选参数 MOTOR_ID_ML/MOTOR_ID_MR</td></tr>
</table>

#### Get_Velocity_From_Encoder(int encoder_left, int encoder_right);
返回左右轮的转速

<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>encoder_left</td><td>int</td><td>左电机编码器值</td></tr>
<tr><td>encoder_right</td><td>int</td><td>右电机编码器值</td></tr>
</table>

<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>velocities</td><td>float*</td></tr>
<tr><td colspan="2">返回值为一个速度数组<br>velocities[0]是左电机速度<br>velocities[1]是右电机速度</td></tr>
</table>



#### TIM3_IRQHandler(void);
定时器3中断处理函数

#### TIM4_IRQHandler(void);
定时器4中断处理函数

