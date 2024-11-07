<style type="text/css">
        body {
            font-family: Arial, sans-serif;
            padding: 20px;
            max-width: 800px;
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
## 蓝牙(Bluetooth)

<div class="notice">
    <p>
        1.bsp_bluetooth.c 文件里存放的是蓝牙基础驱动文件
    </p>
    <p>
        2.app_bluetooth.c 文件里存放的是小车应用蓝牙的文件
    </p>
</div>



### 全局变量

<table border="1">
<tr><th>全局变量</th><th>类型</th><th>注释</th></tr>
<tr><td>g_autoup</td><td>int</td><td>自动上报标志</td></tr>
<tr><td>manydisplay</td><td>char[80]</td><td>上报数据字符串</td></tr>
<tr><td>updata</td><td>char[80]</td><td>存储最终发送的数据</td></tr>
<tr><td>lspeed</td><td>char[10]</td><td>左电机速度字符串</td></tr>
<tr><td>rspeed</td><td>char[10]</td><td>右电机速度字符串</td></tr>
<tr><td>daccel</td><td>char[10]</td><td>加速度字符串</td></tr>
<tr><td>dgyro</td><td>char[10]</td><td>陀螺仪数据字符串</td></tr>
<tr><td>csb</td><td>char[10]</td><td>超声波距离字符串</td></tr>
<tr><td>vi</td><td>char[10]</td><td>电量字符串</td></tr>
<tr><td>newLineReceived</td><td>u8</td><td>新行接收标志</td></tr>
<tr><td>num</td><td>int</td><td>输入字符串长度</td></tr>
<tr><td>startBit</td><td>u8</td><td>协议开始位标志</td></tr>
<tr><td>int9num</td><td>int</td><td>第9个整数值</td></tr>
<tr><td>inputString</td><td>u8[80]</td><td>接收到的输入字符串</td></tr>
<tr><td>ProtocolString</td><td>u8[80]</td><td>协议字符串</td></tr>
<tr><td>g_newcarstate</td><td>enCarState</td><td>小车状态</td></tr>
<tr><td>PID_Original</td><td>float[6]</td><td>PID初始值数组</td></tr>
<tr><td>piddisplay</td><td>char[50]</td><td>PID显示字符串</td></tr>
<tr><td>charkp</td><td>char[10]</td><td>比例增益KP字符串</td></tr>
<tr><td>charkd</td><td>char[10]</td><td>微分增益KD字符串</td></tr>
<tr><td>charksp</td><td>char[10]</td><td>速度环KP字符串</td></tr>
<tr><td>charksi</td><td>char[10]</td><td>速度环KI字符串</td></tr>
<tr><td>charktp</td><td>char[10]</td><td>转向环KP字符串</td></tr>
<tr><td>charktd</td><td>char[10]</td><td>转向环KD字符串</td></tr>
</table>

### 宏定义
<table border="1">
<tr><th>宏定义</th><th>值</th><th>注释</th></tr>
<tr><td>run_car</td><td>'1'</td><td>前进命令</td></tr>
<tr><td>back_car</td><td>'2'</td><td>后退命令</td></tr>
<tr><td>left_car</td><td>'3'</td><td>左转命令</td></tr>
<tr><td>right_car</td><td>'4'</td><td>右转命令</td></tr>
<tr><td>stop_car</td><td>'0'</td><td>停止命令</td></tr>
</table>

### 方法

#### bluetooth_init(void)
初始化蓝牙模块
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### bluetooth_send_char(uint8_t ch)
发送一个字符
<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>ch</td><td>uint8_t</td><td>要发送的字符</td></tr>
</table>
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### UART5_Send_ArrayU8(uint8_t *BufferPtr, uint16_t Length)
发送一个字节数组
<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>BufferPtr</td><td>uint8_t*</td><td>待发送的数据指针</td></tr>
<tr><td>Length</td><td>uint16_t</td><td>数据长度</td></tr>
</table>
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### USART5_Send_Byte(unsigned char byte)
发送一个字节
<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>byte</td><td>unsigned char</td><td>要发送的字节</td></tr>
</table>
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### bluetooth_send_string(char *s)
发送字符串
<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>s</td><td>char*</td><td>待发送的字符串</td></tr>
</table>
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### Init_PID(void)
初始化PID参数
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### ResetPID(void)
恢复开启时的PID参数
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### deal_bluetooth(uint8_t rxbuf)
处理接收到的蓝牙数据
<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>rxbuf</td><td>uint8_t</td><td>接收到的数据</td></tr>
</table>
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### ProtocolCpyData(void)
复制协议数据
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### Protocol(void)
解析协议数据
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### StringFind(const char *pSrc, const char *pDst)
查找子字符串
<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>pSrc</td><td>const char*</td><td>源字符串</td></tr>
<tr><td>pDst</td><td>const char*</td><td>目标字符串</td></tr>
</table>
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>找到的起始索引</td><td>int</td></tr>
</table>

#### CalcUpData(void)
计算和更新上报数据
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### SendAutoUp(void)
定时自动上报数据
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### ProtocolGetPID(void)
获取PID参数
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>


### 使用示例

<div class="code-container">
<pre><code>
<span class="include">#include </span><span class="string">"bsp_bluetooth.h"</span>
<span class="keyword">int </span><span class="function">main</span>() {
    bluetooth_init();
    bluetooth_send_string(<span class="string">"Hello Yahboom!\n"</span>);
    <span class="keyword">while</span>(1);
}
// <span class="comment">当蓝牙接收到消息后会触发该中断</span>
<span class="keyword">void </span><span class="function">UART5_IRQHandler</span>(<span class="keyword">void</span>) {
    uint8_t Rx5_Temp;
    <span class="keyword">if</span> (USART_GetITStatus(UART5, USART_IT_RXNE) != RESET)
    {
        Rx5_Temp = USART_ReceiveData(UART5);
        bluetooth_send_char(Rx5_Temp);
    }
}
</code></pre>
</div>