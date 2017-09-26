# tijos.runtime.deviceaccess - 设备总线

设备总线（deviceaccess），用以控制硬件资源的唯一通道，在TiJOS中传感器（sensor/transducer）类都通过设备总线通道完成对外部硬件的控制，用户可以基于设备总线类编写标准库中未提供的传感器类。



TiJOS 设备总线包括如下类：

| 类名          | 说明                                       |      |
| ----------- | ---------------------------------------- | ---- |
| TiGPIO      | [通用输入/输出（General Purpose Input Output ）](tijos.runtime.deviceaccess.TiGPIO.md) |      |
| TiUART      | [通用异步收发传输器（Universal Asynchronous Receiver/Transmitter](tijos.runtime.deviceaccess.TiUART.md) |      |
| TiADC       | [模数转换器（ Analog-to-Digital Converter）](tijos.runtime.deviceaccess.TiADC.md) |      |
| TiPWM       | [脉冲宽度调制发生器（ Pulse Width Modulation）](tijos.runtime.deviceaccess.TiPWM.md) |      |
| TiI2CMaster | [双向二线制同步串行总线（ Inter-Integrated Circuit），主机模式 ](tijos.runtime.deviceaccess.TiI2CMaster.md) |      |
| TiSPIMaster | [串行外设接口 （Serial Peripheral Interface），主机模式](tijos.runtime.deviceaccess.TiSPIMaster.md) |      |
| TiOWMaster  | [单总线（one wire），主机模式](tijos.runtime.deviceaccess.TiOWMaster.md) |      |


