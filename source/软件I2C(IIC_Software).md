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
## 软件I2C(IIC_Software)

### 方法
#### IIC_MPU6050_Init()
IIC引脚初始化
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### IIC_Start()
模拟IIC起始信号
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>1</td><td>int</td></tr>
</table>

#### IIC_Stop()
模拟IIC结束信号
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### IIC_Wait_Ack()
IIC等待应答信号
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>0：没有收到应答；1：收到应答</td><td>int</td></tr>
</table>

#### IIC_Ack()
IIC应答
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### IIC_NAck()
IIC不应答
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### IIC_Send_Byte(u8 txd)
IIC发送一个字节
<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>txd</td><td>u8</td><td>发送的字节数据</td></tr>
</table>
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>无</td><td>void</td></tr>
</table>

#### i2cWrite(uint8_t addr, uint8_t reg, uint8_t len, uint8_t *data)
IIC写数据到寄存器
<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>addr</td><td>uint8_t</td><td>设备地址</td></tr>
<tr><td>reg</td><td>uint8_t</td><td>寄存器地址</td></tr>
<tr><td>len</td><td>uint8_t</td><td>字节数</td></tr>
<tr><td>data</td><td>uint8_t*</td><td>数据</td></tr>
</table>
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>0：成功写入；1：没有成功写入</td><td>int</td></tr>
</table>

#### i2cRead(uint8_t addr, uint8_t reg, uint8_t len, uint8_t *buf)
IIC读寄存器的数据
<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>addr</td><td>uint8_t</td><td>设备地址</td></tr>
<tr><td>reg</td><td>uint8_t</td><td>寄存器地址</td></tr>
<tr><td>len</td><td>uint8_t</td><td>字节数</td></tr>
<tr><td>buf</td><td>uint8_t*</td><td>读出数据缓存</td></tr>
</table>
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>0：成功读出；1：没有成功读出</td><td>int</td></tr>
</table>

#### IIC_Read_Byte(unsigned char ack)
IIC读取一个字节
<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>ack</td><td>unsigned char</td><td>是否发送应答信号；1：发送；0：不发送</td></tr>
</table>
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>receive：读取的数据</td><td>u8</td></tr>
</table>

#### I2C_ReadOneByte(unsigned char I2C_Addr, unsigned char addr)
读取指定设备指定寄存器的一个值
<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>I2C_Addr</td><td>unsigned char</td><td>设备IIC地址</td></tr>
<tr><td>addr</td><td>unsigned char</td><td>寄存器地址</td></tr>
</table>
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>res：读取的数据</td><td>unsigned char</td></tr>
</table>

#### IICreadBytes(u8 dev, u8 reg, u8 length, u8 *data)
IIC连续读数据
<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>dev</td><td>u8</td><td>目标设备IIC地址</td></tr>
<tr><td>reg</td><td>u8</td><td>寄存器地址</td></tr>
<tr><td>length</td><td>u8</td><td>字节数</td></tr>
<tr><td>data</td><td>u8*</td><td>读出的数据将要存放的指针</td></tr>
</table>
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>count：读出来的字节数量-1</td><td>u8</td></tr>
</table>

#### IICwriteBytes(u8 dev, u8 reg, u8 length, u8* data)
将多个字节写入指定设备指定寄存器
<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>dev</td><td>u8</td><td>目标设备地址</td></tr>
<tr><td>reg</td><td>u8</td><td>寄存器地址</td></tr>
<tr><td>length</td><td>u8</td><td>要写的字节数</td></tr>
<tr><td>data</td><td>u8*</td><td>将要写的数据的首地址</td></tr>
</table>
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>1：返回是否成功</td><td>u8</td></tr>
</table>

#### IICreadByte(u8 dev, u8 reg, u8 *data)
读取指定设备指定寄存器的一个值
<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>dev</td><td>u8</td><td>目标设备地址</td></tr>
<tr><td>reg</td><td>u8</td><td>寄存器地址</td></tr>
<tr><td>data</td><td>u8*</td><td>读出的数据将要存放的指针</td></tr>
</table>
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>1：返回是否成功</td><td>u8</td></tr>
</table>

#### IICwriteByte(unsigned char dev, unsigned char reg, unsigned char data)
写入指定设备指定寄存器一个字节
<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>dev</td><td>unsigned char</td><td>目标设备地址</td></tr>
<tr><td>reg</td><td>unsigned char</td><td>寄存器地址</td></tr>
<tr><td>data</td><td>unsigned char</td><td>发送的字节数据</td></tr>
</table>
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>1：返回是否成功</td><td>u8</td></tr>
</table>

#### IICwriteBits(u8 dev, u8 reg, u8 bitStart, u8 length, u8 data)
读、修改、写指定设备指定寄存器一个字节中的多个位
<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>dev</td><td>u8</td><td>目标设备地址</td></tr>
<tr><td>reg</td><td>u8</td><td>寄存器地址</td></tr>
<tr><td>bitStart</td><td>u8</td><td>目标字节的起始位</td></tr>
<tr><td>length</td><td>u8</td><td>目标字节的位数</td></tr>
<tr><td>data</td><td>u8</td><td>存放改变目标字节位的值</td></tr>
</table>
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>1：成功；0：失败</td><td>u8</td></tr>
</table>

#### IICwriteBit(u8 dev, u8 reg, u8 bitNum, u8 data)
读、修改、写指定设备指定寄存器一个字节中的1个位
<table border="1">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
<tr><td>dev</td><td>u8</td><td>目标设备地址</td></tr>
<tr><td>reg</td><td>u8</td><td>寄存器地址</td></tr>
<tr><td>bitNum</td><td>u8</td><td>要修改目标字节的bitNum位</td></tr>
<tr><td>data</td><td>u8</td><td>为0时，目标位将被清，否则将被置位</td></tr>
</table>
<table border="1">
<tr><th>返回值</th><th>类型</th></tr>
<tr><td>1：成功；0：失败</td><td>u8</td></tr>
</table>