# STM32 PID恒温控制系统

## 简介

本资源文件提供了一个基于STM32的PID恒温控制系统的设计与实现。该系统利用DHT11传感器检测环境温湿度，并通过PID算法控制加热丝的PWM输出，实现温度的稳定控制。系统还包括L298N模块、LCD1602显示、蜂鸣器报警等功能。

## 功能描述

1. **温湿度检测**：使用DHT11传感器实时检测环境的温湿度，并将数据显示在LCD1602上。
2. **PID控制**：通过PID算法计算出当前输出脉宽，并将其加在L298N模块中，使加热丝发热，形成一个闭环控制系统。
3. **温度稳定**：经过一段时间后，系统能够将温度稳定在设定值。
4. **湿度报警**：当环境湿度超出设定范围时，蜂鸣器会发出报警信号。

## 系统组成

- **STM32F103核心板**：作为控制核心。
- **DHT11传感器**：用于检测环境温湿度。
- **L298N模块**：用于驱动加热丝。
- **LCD1602显示屏**：用于显示当前温湿度数据。
- **蜂鸣器**：用于湿度报警。

## 工作原理

1. **温湿度采集**：DHT11传感器每隔一段时间采集一次温湿度数据，并将数据传输给STM32。
2. **PID计算**：STM32根据设定温度与当前温度的差值，通过PID算法计算出PWM的占空比。
3. **加热控制**：根据计算出的PWM占空比，控制L298N模块驱动加热丝，使其发热或停止发热。
4. **显示与报警**：LCD1602显示当前温湿度数据，当湿度超出设定范围时，蜂鸣器发出报警信号。

## 使用说明

1. **硬件连接**：按照原理图连接各硬件模块。
2. **软件配置**：将提供的代码烧录到STM32核心板中。
3. **参数调整**：根据实际需求调整PID控制器的比例、积分和微分系数。
4. **运行测试**：启动系统，观察温湿度数据及报警情况。

## 注意事项

- 确保所有硬件连接正确，避免短路或接触不良。
- 在调整PID参数时，需根据实际环境进行多次测试，以达到最佳控制效果。
- 系统运行时，注意观察加热丝的温度，避免过热。

## 参考资料

- [PID控制算法基础](https://zh.wikipedia.org/wiki/PID控制器)
- [STM32开发指南](https://www.st.com/content/st_com/zh/products/microcontrollers-microprocessors/stm32-32-bit-arm-cortex-mcus.html)

## 作者

- 浪客小子

## 版权声明

本项目遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接和本声明。

## 下载链接

[STM32PID恒温控制系统](https://pan.quark.cn/s/da5fb82f877d)