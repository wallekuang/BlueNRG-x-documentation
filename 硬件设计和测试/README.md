# 硬件设计和测试

下文描述了硬件设计和硬件测试的参考资料，希望给加速硬件工程师对BlueNRG-系列芯片进行硬件设计和测试。

## 硬件设计

### BlueNRG-x 原理图和Layout:

#### 参考文档：

[参考文档](https://www.st.com/resource/en/application_note/dm00718453-pcb-design-guidelines-for-the-bluenrglp-device-stmicroelectronics.pdf)[: PCB design guidelines for the BlueNRG-LP device Application Note (AN5526) ](https://www.st.com/resource/en/application_note/dm00718453-pcb-design-guidelines-for-the-bluenrglp-device-stmicroelectronics.pdf)

[参考文档](https://www.st.com/resource/en/application_note/dm00263000.pdf)[: PCB design guidelines for the BlueNRG-1,2 device Application Note (AN4819) ](https://www.st.com/resource/en/application_note/dm00263000.pdf)

#### 参考layout：

##### [BlueNRG-X_Layout参考](BlueNRG-X_Layout参考/README.md)



## 硬件测试

制作PCBA后，需要对硬件进行测试，一般测试包括如下项目。

- 电源测试
- 应用PCBA测试点
- 低速晶振（32K）
- 高速晶振起震时间
- RF测试
  - 非信令测试
    - 发射功率
    - 接收灵敏度
    - 频偏 （高速晶振）
  - 信令模式



RF测试测试需要烧录DTM固件，结合使用GUI工具和测试仪器进行测试。

### 硬件测试参考文档

[Bringing up the BlueNRG-LP device Application Note (AN5503) ](https://www.st.com/resource/en/application_note/dm00710278-bringing-up-the-bluenrglp-device-stmicroelectronics.pdf)

[Bringing up the BlueNRG-1,2 device Application Note (AN4818) ](https://www.st.com/resource/en/application_note/dm00262995.pdf)

