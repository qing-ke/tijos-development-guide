# TiJOS JDK Runtime 包说明

TiJOS JDK中另一大部分Runtime类供用户在应用中对硬件资源及传感器类等进行操作, 其中包括对各种硬件接口和传感器类的操作， 同时也提供了一些可能用到的工具类, 如BASE64, JSON等等



## Runtime 子模块说明

| 包名称                             | 说明                                       |
| ------------------------------- | ---------------------------------------- |
| tijos.runtime.platform          | 系统设置相关类，主机名称等设置                          |
| tijos.runtime.eventcenter       | 事件中心类，处理来自硬件外设总线的事件，如GPIO事件等             |
| tijos.runtime.networkcenter     | 网络中心类，管理网络相关配置及状态等，如：WLAN、DNS等           |
| tijos.runtime.deviceaccess      | 设备总线相关类，如GPIO, I2C, PWM等等，可用来开发在标准库中不支持的传感器 |
| tijos.runtime.sensor.button     | 按键类                                      |
| tijos.runtime.sensor.distance   | 测距类                                      |
| tijos.runtime.sensor.gas        | 气体传感类                                    |
| tijos.runtime.sensor.humiture   | 温湿度传感类                                   |
| tijos.runtime.sensor.infrared   | 红外线类                                     |
| tijos.runtime.transducer.buzzer | 蜂鸣类                                      |
| tijos.runtime.transducer.led    | LED显示类                                   |
| tijos.runtime.transducer.relay  | 继电器类                                     |
| tijos.runtime.net.ntp           | 网络时间协议客户端                                |
| tijos.runtime.net.mqtt          | MQTT 客户端，支持3.1.1标准                       |
| tijos.runtime.ota               | 应用在线升级类                                  |
| tijos.util.base64               | BASE64转换类                                |
| tijos.util.json                 | JSON 处理类                                 |
| tijos.util.logging              | 日志类，输出到打印口                               |

