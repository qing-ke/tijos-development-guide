# TiJOS 常用工具类使用说明

为了方便用户使用， TiJOS 提供了一些常用的工具类方便用户在应用中使用， 如日志，BASE64，JSON等。

| 类                  | 说明        |
| ------------------ | --------- |
| tijos.util.base64  | BASE64编码类 |
| tijos.util.json    | JSON类     |
| tijos.util.logging | 日志类       |
| tijos.util.crc     | CRC校验码    |

## BASE64

BASE64是网络上最常见的使用字符串传输8位字节码的编码方式，具体请参考tijos.util.base64相关说明。

## JSON

JSON是一种常用的数据交换方式，也是物联网云服务使用最多数据格式， TiJOS 提供JSON类可以很方便将Key-Value数据组装为JSON格式发送到其它应用进行数据交换， 具体请参考tijos.util.json相关说明。

## Logging 

日志类用于控制日志的输出, 可通过设置动态调整输出日志级别， 具体请参考tijos.util.logging。

## CRC

CRC是一种数据通讯过程中常用的校验码运算方式，TiJOS提供了支持CRC8和CRC16, 具体请参考tijos.util.crc相关说明。