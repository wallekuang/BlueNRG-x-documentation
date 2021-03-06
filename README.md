# BlueNRG-x-documentation


# 建议转到链接：https://gitee.com/lucienkuang/BlueNRG-x-documentation

## 前言 
- 本仓库是由个人维护的一个ST BlueNRG系列（BLE芯片）非正式文档的主页。
  主要包含： 
    - 1.平时培训文档; 
    - 2.快速上手资料；
    - 3.客户常见问题分析与总结；
    - 4.BLE协议教程；
    - 5.一些典型应用的参考设计。
- 建议尽可能使用最新版本的SDK。
- 文档主要是用markdown格式编写的，可以使用VScode或者Typora等支持markdown格式的编辑器打开。
- 建议大陆用户使用这个链接: https://gitee.com/lucienkuang/BlueNRG-x-documentation
  或者没有更改host，可能无法直接在线加载查看到图片信息。
- 下载与更新：
  - 下载: git clone https://github.com/wallekuang/BlueNRG-x-documentation.git
  - 更新:  git pull
- 如果文档查看相关文档仍然无法解决您的问题，或者想进一步交流，也可以直接发邮件到： lucien.kuang@st.com  或者在GitHub的此仓库上提issues
- 有问题也可发表到论坛： http://bbs.eeworld.com.cn/forum-262-1.html 也会有工程师进行解答



## 目录
- [快速开始与开发环境搭建](Quickstart/README.md)
  - [资料下载与软件安装](Quickstart/资料下载与软件安装.md)
  - [官方主要资料查找](Quickstart/官方主要资料查找.md)
  - [认识BlueNRG-LP的评估板](Quickstart/认识BlueNRG-LP的评估板.md)


- [硬件设计和测试](硬件设计和测试/README.md)
- [BLE协议基础](BLE/README.md)
- [BLE协议栈进阶](BLE/BLE协议栈基础.md)
  - 数据扩展包
  - BLE安全
  - 蓝牙5.0之扩展广播
- [常见应用](Application/README.md)
  <details>
  <summary>常见应用展开</summary>

  - [如何优化BlueNRG-x的功耗](Application/功耗优化/如何优化BlueNRG-x的功耗.md)
  - [基于BLE多连接的星型网络应用](Application/Multiple_connection/基于BLE多连接的星型网络应用.md) 

   - [BlueNRG系列存储分析(Flash_and_RAM)](Application/BlueNRG系列如何使用静态协议栈/BlueNRG系列存储分析(Flash_and_RAM).MD) 
  - [BlueNRG系列如何使用静态协议栈](Application/BlueNRG系列如何使用静态协议栈/BlueNRG系列如何使用静态协议栈.MD)
  - [BlueNRG系列的OTA](Application/OTA/BlueNRG-x系列官方OTA操作简介.md)
  - BlueNRG系列协处理器介绍
  - BlueNRG系列中使用FreeRTOS

  </details>

- [工具使用](工具使用/README.md)

  - [开源改进的版本的Flasher_utility下载工具](https://github.com/wallekuang/MP-Tool)
- [FAQ](FAQ/README.md)
  <details>
   <summary>FAQ展开</summary>

  - [如何区分不同的DTM工程与配置](FAQ/AboutDTM/关于BlueNRG-LP的DTM.md)
  - [如何查找QDID](FAQ/如何查找QDID.md)
  - [BlueNRG-x系列如何简单延时](FAQ/BlueNRG系列如何简单的延时.md)
  - [如何安装GNU工具链](FAQ/安装GNU工具链/如何安装GNU工具链.md)
  - [BlueNRG-1-2睡眠模式下使用RTC](FAQ/BlueNRG-1-2睡眠模式下使用RTC.md)
  - [如何在SDK中适配使用BlueNRG-345](FAQ/使用BlueNRG-345注意事项.md)
  - [如何设定BlueNRG系列广播数据](FAQ/如何设定广播数据.md)
  - [BlueNRG-LP如何在Radio_TX或者RX时将某个GPIO置位高电平_or_如何软件配置控制外部PA的TX和RX](FAQ/RadioTXRX_map_to_gpio/如何在Radio_TX或者RX时将某个GPIO置位高电平.md)

  </details>

- [培训资料](培训资料/README.md)
  - [2021_04_08_level1_BlueNRG系列培训资料](培训资料/2021_04_08_level1)





