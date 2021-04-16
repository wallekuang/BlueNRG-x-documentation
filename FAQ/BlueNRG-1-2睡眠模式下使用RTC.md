# BlueNRG-1-2睡眠模式下使用RTC

BlueNRG-1/2在睡眠模式下，硬件RTC是关闭不可用的。为了方便用户，这里写了一个基于32K时钟进行模拟的RTC驱动。

源码链接如下：

https://github.com/wallekuang/BlueNRG_Demo/tree/master/BlueNRG-1_2%20DK%203.1.0/Project/Supply/BLE_RTC



1个tick为 625/256 us.  // 蓝牙时钟基础

409600 个tick 刚好是1秒

HAL_VTimerGetCurrentTime_sysT32  获取的值是一个不断增加的数值(tick)，当增加到0XFFFFFFFF后又从0开始递增。