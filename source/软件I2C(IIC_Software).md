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
</style>
## 软件I2C(IIC_Software)

<div class="notice">
    <p>该驱动库位于 <br> MPU6050/IIC_Software </br> 目录下，在小车中仅用于做MPU6050的通信支持</p>
</div>


### 方法
#### IIC_MPU6050_Init()
MPU6050的IIC引脚初始化
<table>
<thead class="table100-head">
<tr><th>返回值</th><th>类型</th></tr>
</thead>
<tbody>
    <tr><td>无</td><td>void</td></tr>
</tbody>
</table>

#### IIC_Start()
模拟IIC起始信号
<table>
<thead class="table100-head">
<tr><th>返回值</th><th>类型</th></tr>
</thead>
<tbody>
    <tr><td>1</td><td>int</td></tr>
</tbody>
</table>

#### IIC_Stop()
模拟IIC结束信号
<table>
<thead class="table100-head">
<tr><th>返回值</th><th>类型</th></tr>
</thead>
<tbody>
    <tr><td>无</td><td>void</td></tr>
</tbody>
</table>

#### IIC_Wait_Ack()
IIC等待应答信号
<table>
<thead class="table100-head">
<tr><th>返回值</th><th>类型</th></tr>
</thead>
<tbody>
    <tr><td>0：没有收到应答；1：收到应答</td><td>int</td></tr>
</tbody>
</table>

#### IIC_Ack()
IIC应答
<table>
<thead class="table100-head">
<tr><th>返回值</th><th>类型</th></tr>
</thead>
<tbody>
    <tr><td>无</td><td>void</td></tr>
</tbody>
</table>

#### IIC_NAck()
IIC不应答
<table>
<thead class="table100-head">
<tr><th>返回值</th><th>类型</th></tr>
</thead>
<tbody>
    <tr><td>无</td><td>void</td></tr>
</tbody>
</table>

#### IIC_Send_Byte(u8 txd)
IIC发送一个字节
<table>
<thead class="table100-head">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
</thead>
<tbody>
    <tr><td>txd</td><td>u8</td><td>发送的字节数据</td></tr>
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

#### i2cWrite(uint8_t addr, uint8_t reg, uint8_t len, uint8_t *data)
IIC写数据到寄存器
<table>
<thead class="table100-head">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
</thead>
<tbody>
    <tr><td>addr</td><td>uint8_t</td><td>设备地址</td></tr>
<tr><td>reg</td><td>uint8_t</td><td>寄存器地址</td></tr>
<tr><td>len</td><td>uint8_t</td><td>字节数</td></tr>
<tr><td>data</td><td>uint8_t*</td><td>数据</td></tr>
</tbody>
</table>
<table>
<thead class="table100-head">
<tr><th>返回值</th><th>类型</th></tr>
</thead>
<tbody>
    <tr><td>0：成功写入；1：没有成功写入</td><td>int</td></tr>
</tbody>
</table>

#### i2cRead(uint8_t addr, uint8_t reg, uint8_t len, uint8_t *buf)
IIC读寄存器的数据
<table>
<thead class="table100-head">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
</thead>
<tbody>
    <tr><td>addr</td><td>uint8_t</td><td>设备地址</td></tr>
<tr><td>reg</td><td>uint8_t</td><td>寄存器地址</td></tr>
<tr><td>len</td><td>uint8_t</td><td>字节数</td></tr>
<tr><td>buf</td><td>uint8_t*</td><td>读出数据缓存</td></tr>
</tbody>
</table>
<table>
<thead class="table100-head">
<tr><th>返回值</th><th>类型</th></tr>
</thead>
<tbody>
    <tr><td>0：成功读出；1：没有成功读出</td><td>int</td></tr>
</tbody>
</table>

#### IIC_Read_Byte(unsigned char ack)
IIC读取一个字节
<table>
<thead class="table100-head">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
</thead>
<tbody>
    <tr><td>ack</td><td>unsigned char</td><td>是否发送应答信号；1：发送；0：不发送</td></tr>
</tbody>
</table>
<table>
<thead class="table100-head">
<tr><th>返回值</th><th>类型</th></tr>
</thead>
<tbody>
    <tr><td>receive：读取的数据</td><td>u8</td></tr>
</tbody>
</table>

#### I2C_ReadOneByte(unsigned char I2C_Addr, unsigned char addr)
读取指定设备指定寄存器的一个值
<table>
<thead class="table100-head">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
</thead>
<tbody>
    <tr><td>I2C_Addr</td><td>unsigned char</td><td>设备IIC地址</td></tr>
<tr><td>addr</td><td>unsigned char</td><td>寄存器地址</td></tr>
</tbody>
</table>
<table>
<thead class="table100-head">
<tr><th>返回值</th><th>类型</th></tr>
</thead>
<tbody>
    <tr><td>res：读取的数据</td><td>unsigned char</td></tr>
</tbody>
</table>

#### IICreadBytes(u8 dev, u8 reg, u8 length, u8 *data)
IIC连续读数据
<table>
<thead class="table100-head">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
</thead>
<tbody>
    <tr><td>dev</td><td>u8</td><td>目标设备IIC地址</td></tr>
<tr><td>reg</td><td>u8</td><td>寄存器地址</td></tr>
<tr><td>length</td><td>u8</td><td>字节数</td></tr>
<tr><td>data</td><td>u8*</td><td>读出的数据将要存放的指针</td></tr>
</tbody>
</table>
<table>
<thead class="table100-head">
<tr><th>返回值</th><th>类型</th></tr>
</thead>
<tbody>
    <tr><td>count：读出来的字节数量-1</td><td>u8</td></tr>
</tbody>
</table>

#### IICwriteBytes(u8 dev, u8 reg, u8 length, u8* data)
将多个字节写入指定设备指定寄存器
<table>
<thead class="table100-head">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
</thead>
<tbody>
    <tr><td>dev</td><td>u8</td><td>目标设备地址</td></tr>
<tr><td>reg</td><td>u8</td><td>寄存器地址</td></tr>
<tr><td>length</td><td>u8</td><td>要写的字节数</td></tr>
<tr><td>data</td><td>u8*</td><td>将要写的数据的首地址</td></tr>
</tbody>
</table>
<table>
<thead class="table100-head">
<tr><th>返回值</th><th>类型</th></tr>
</thead>
<tbody>
    <tr><td>1：返回是否成功</td><td>u8</td></tr>
</tbody>
</table>

#### IICreadByte(u8 dev, u8 reg, u8 *data)
读取指定设备指定寄存器的一个值
<table>
<thead class="table100-head">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
</thead>
<tbody>
    <tr><td>dev</td><td>u8</td><td>目标设备地址</td></tr>
<tr><td>reg</td><td>u8</td><td>寄存器地址</td></tr>
<tr><td>data</td><td>u8*</td><td>读出的数据将要存放的指针</td></tr>
</tbody>
</table>
<table>
<thead class="table100-head">
<tr><th>返回值</th><th>类型</th></tr>
</thead>
<tbody>
    <tr><td>1：返回是否成功</td><td>u8</td></tr>
</tbody>
</table>

#### IICwriteByte(unsigned char dev, unsigned char reg, unsigned char data)
写入指定设备指定寄存器一个字节
<table>
<thead class="table100-head">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
</thead>
<tbody>
    <tr><td>dev</td><td>unsigned char</td><td>目标设备地址</td></tr>
<tr><td>reg</td><td>unsigned char</td><td>寄存器地址</td></tr>
<tr><td>data</td><td>unsigned char</td><td>发送的字节数据</td></tr>
</tbody>
</table>
<table>
<thead class="table100-head">
<tr><th>返回值</th><th>类型</th></tr>
</thead>
<tbody>
    <tr><td>1：返回是否成功</td><td>u8</td></tr>
</tbody>
</table>

#### IICwriteBits(u8 dev, u8 reg, u8 bitStart, u8 length, u8 data)
读、修改、写指定设备指定寄存器一个字节中的多个位
<table>
<thead class="table100-head">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
</thead>
<tbody>
    <tr><td>dev</td><td>u8</td><td>目标设备地址</td></tr>
<tr><td>reg</td><td>u8</td><td>寄存器地址</td></tr>
<tr><td>bitStart</td><td>u8</td><td>目标字节的起始位</td></tr>
<tr><td>length</td><td>u8</td><td>目标字节的位数</td></tr>
<tr><td>data</td><td>u8</td><td>存放改变目标字节位的值</td></tr>
</tbody>
</table>
<table>
<thead class="table100-head">
<tr><th>返回值</th><th>类型</th></tr>
</thead>
<tbody>
    <tr><td>1：成功；0：失败</td><td>u8</td></tr>
</tbody>
</table>

#### IICwriteBit(u8 dev, u8 reg, u8 bitNum, u8 data)
读、修改、写指定设备指定寄存器一个字节中的1个位
<table>
<thead class="table100-head">
<tr><th>参数</th><th>类型</th><th>注释</th></tr>
</thead>
<tbody>
    <tr><td>dev</td><td>u8</td><td>目标设备地址</td></tr>
<tr><td>reg</td><td>u8</td><td>寄存器地址</td></tr>
<tr><td>bitNum</td><td>u8</td><td>要修改目标字节的bitNum位</td></tr>
<tr><td>data</td><td>u8</td><td>为0时，目标位将被清，否则将被置位</td></tr>
</tbody>
</table>
<table>
<thead class="table100-head">
<tr><th>返回值</th><th>类型</th></tr>
</thead>
<tbody>
    <tr><td>1：成功；0：失败</td><td>u8</td></tr>
</tbody>
</table>

