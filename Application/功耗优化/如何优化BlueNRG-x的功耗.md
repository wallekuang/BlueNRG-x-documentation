## 如何优化BlueNRG-x的功耗  

  如何优化功耗，这是一个比较大的话题。这里简单说一下。

1. 硬件层面的优化（使用内部DC-DC）,Radio运作时使用内部DCDC功耗是不使用的一半。

   <img src=".\dcdc.png" alt="dcdc" style="zoom:38%;" />

2. 对功耗有个基本的大致评估预算（包括各个状态，睡眠广播连接等）。

   使用BlueNRG Current Consumption Estimation Tool 工具对各种状态大致评估。

   <img src=".\BlueNRG Current Consumption Estimation Tool.png" alt="BlueNRG Current Consumption Estimation Tool" style="zoom:38%;" />

   <img src="E:\Work\2019\summary\workshow_lucien\FQA\常见应用\功耗优化\sleep.png" alt="sleep" style="zoom:38%;" />

3. 实际抓电流波形分析，各个状态和步骤2是否符合预估值， 不符合则排查软硬件。

   <img src=".\RT power comsumption.png" alt="RT power comsumption" style="zoom:38%;" />

4. 对于睡眠电流如果测试到1.3uA左右，不是预估的0.9uA，那么可能需要设置一下。

   LL_RCC_LSE_SetDriveCapability(LL_RCC_LSEDRIVE_LOW)

   这个函数主要时决定睡眠时是否关闭RTC和看门狗等，如果选择关闭会比之前不关闭大概少300~400nA.

5. 其他建议:

   a. 尽可能让程序多睡眠

   b. 尽可能让程序少唤醒（可以让多个软件定时器和BLE事件等处于同一个周期能减少唤醒次数）

   c. 优化程序应用设计。