# tijos.framework.ota - 在线应用升级

OTA 英文全称是Over-the-Air Technology，即空间下载技术的意思。TiJOS为用户提供了OTA的基础功能，如：应用的写入、安装、校验等。用户可根据实际应用的需要通过不同方式，如：无线WIFI等，进行应用的在线升级，TiJOS提供的OTA功能具有升级失败自动回滚特性，保证用户应用不会被损坏。



包含类如下:

| 类名                | 说明      |
| ----------------- | ------- |
| TiOTA             | OTA类    |
| TiOTAOutputStream | OTA流操作类 |



主要方法如下：

| 构造器、方法                            | 说明      |
| --------------------------------- | ------- |
| TiOTA()                           | OTA实例创建 |
| OutputStream getOTAOutputStream() | 获取流操作实例 |
| int install()                     | 安装应用    |



调用过程如下所示：

```java
...
...
TiOTA ota = new TiOTA(); 						//创建OTA实例
OutputStream stream = ota.getOTAOutputStream();	  //获取流操作实例
...
stream.write(transBuffer, 0, transLength);		  //流写入
...
int status = ota.install();						 //应用安装
if(status == 0)
	System.exit(0);                               //此处可调用系统退出，程序会重新启动
...
...
```



TiOTA详细使用方法请参考TiOTA在线应用升级功能例程。