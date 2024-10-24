## 电池电压(Battery)

**标*号的方法为不常用方法**

### 方法
#### Battery_init()
初始化电池电压测量库

#### Get_Battery_Volotage(void)
*注：Yahboom STM32平衡小车配的电源电压输出范围大致在 8.5~12.5v之间*

获得实际电池分压前电压<br>
实际测量的值比计算得出的值低一点点<br><br>
| 返回值 | 类型 |<br>
| 原始电压值 | float |<br>


#### *Battery_Get(uint8_t ch)
获取ADC测量值<br><br>
| 参数  | 类型 | 注释   |<br>
| ch | uint8_t | ADC通道 |<br>

| 返回值 | 类型 |<br>
| 获取到的ADC值 | uint16_t |<br>

#### *Battery_Get_Average(uint8_t ch, uint8_t times)
获得 ADC 多次测量平均值 <br><br>
| 参数  | 类型 | 注释   |<br>
| ch | uint8_t | ADC通道 |<br>
|times| uint8_t | 测量次数 |<br>

#### *Get_Measure_Volotage(void)
获得测得原始电压值<br><br>

| 返回值 | 类型 |<br>
| 原始电压值 | float |<br>

