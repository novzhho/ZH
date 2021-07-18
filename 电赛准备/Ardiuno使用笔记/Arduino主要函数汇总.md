# Arduino学习中的笔记
[本笔记内容均来自于太极创客](http://www.taichi-maker.com/)
## 主要函数及使用方法（持续更新）

### 1.引脚电平状态读写
    digitalRead(val)：读引脚电平状态的函数  
    digitalWrite(val)：写引脚电平状态的函数

### 2.PWM输出函数
PWM:通过改变占空比来调节例如LED灯的亮度或者改变电机动力

    analogWrite(pin,val):模拟输出函数  
        Uno控制器支持引脚3，5，6，9，10，11  
        pin: 被读取的模拟引脚号码  
        val:0-255之间的PWM频率值，0对应off，255对应on

### 3.模拟输入函数
    analogRead(pin)：从Arduino的模拟输入引脚读取数值
	    pin:被读取的模拟引脚号码
        返回值为0-1023

#### 3.1 模拟输入0-1023可等比映射为0-255
    map(x,in_min,in_max,out_min,out_max):等比映射
        x： 要映射的值
	    in_min:映射前区间最小值
	    in_max:映射前区间最大值
	    out_min:映射后区间最小值
        out_max:映射后区间最大值

### 4.引脚状态定义函数
    pinMode(pin，state)：将引脚设置为输入或输出
	    • 输出(OUTPUT)模式
	    • 输入(INPUT)模式
	    • 输入上拉（INPUT_PULLUP）模式
