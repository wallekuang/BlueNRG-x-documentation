## BlueNRG-x系列如何简单延时

​    在写应用代码时，经常需要用到延时函数，如果没有使用RTOS系统，毫秒级别的延时其实不建议使用阻塞类型的延时，建议采用异步非阻塞型。

​    下面分别举例子延时1秒周期用串口打印一个*号：

### BlueNRG-LP 系列:  

```c
void sys_alive_detect(void)
{
  static uint64_t last_time = 0;
  // 获取当前系统时间，只要软件定时器不关闭，这个系统时间会一直运行，睡眠也可以用 ，一个tick的时间单位为625/256
  uint64_t cur_time = TIMER_GetCurrentSysTime();
  uint64_t time_gap =  (uint64_t)((cur_time - last_time)*2.4414/1000);

  if(time_gap > 1000){
    last_time = cur_time;
    printf("*");
  }
}
```

### BlueNRG-1/2 系列:

```c++
void sys_alive_detect(void)
{
  static uint32_t last_time = 0;
  // 获取当前系统时间，只要软件定时器不关闭，这个系统时间会一直运行，睡眠也可以用 ，一个tick的时间单位为625/256
  uint32_t cur_time = HAL_VTimerGetCurrentTime_sysT32();
  uint32_t time_gap =  (uint32_t)((cur_time - last_time)*2.4414/1000);

  if(time_gap > 1000){
    last_time = cur_time;
    printf("*");
  }
}
```



同步类型的延时一半要求时间短，当然也可以用获取系统时间来做，选择的时间基准相对多一些选择，可以用systick，或者基于硬件定时器或者其他。

### BlueNRG-1/2 系列同步延时参考代码:

```c
#include<stdlib.h>
void delay_ms(uint32_t ms)
{
		uint32_t last_tick = HAL_VTimerGetCurrentTime_sysT32();
		uint32_t elapsed_time = 0;
		uint32_t delay_tick = (uint32_t)(ms*1000/2.4414);
		while(elapsed_time < delay_tick){
				uint32_t cur_tick = HAL_VTimerGetCurrentTime_sysT32();
				elapsed_time = abs(cur_tick - last_tick);
				__NOP();
		}		
}
```

