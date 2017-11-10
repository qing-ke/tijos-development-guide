# tijos.framework.platform - 平台设置

tijos.framework.platform中包含了与平台设置相关的类，主机名称，电源管理等等， 这些设置可通过Ti-DevManager工具进行设置，也可通过tijos.framework.platform中的相关类和接口进行设置。

包含类如下:

| 类名称        | 说明         |
| ---------- | ---------- |
| TiPowerMgr | 电源管理       |
| TiSettings | 系统设置，如主机名称 |



## TiPowerMgr

主要方法如下：

| 方法                                       | 说明                                       |
| ---------------------------------------- | ---------------------------------------- |
| void hibernate(int timeWakeup)           | 系统进入冬眠模式，并在指定时间后自动唤醒，时间单位：秒。**唤醒后程序会重新运行**。 |
| void hibernate(TiGPIO gpio, int wakeupPinID) | 系统进入冬眠模式，并通过指定gpio的pin唤醒。**唤醒后程序会重新运行**。 |
| void standby(TiGPIO gpio, int wakeupPinID) | 系统进入待机模式，并通过指定gpio的pin唤醒。 **唤醒后程序会继续运行**。 |

TiPowerMgr类中他方法的技术说明请参考TiJOS Framework说明文档。

注意：电源管理受平台特性限制，设置时须了解硬件平台特性。



调用过程举例：

```java
...
TiPowerMgr.hibernate(60); //系统进入冬眠模式，并在60秒以后自动唤醒。
...
```



## TiSettings

主要方法如下：

| 方法                             | 说明       |
| ------------------------------ | -------- |
| void hostRename(String name)   | 主机重命名    |
| void setLoggerLevel(int level) | 设置全局日志等级 |

TiSettings类中他方法的技术说明请参考TiJOS Framework说明文档。



调用过程举例：

```java
...
TiSettings.hostRename("TiJOS-12345678"); //重新命名主机名
...
TiSettings.setLoggerLevel(1000); //设置全局日志等级为1000
...
```

