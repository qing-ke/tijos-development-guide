# 概述

Ti-Dev Studio是由钛云物联基于Eclipse开发的一款插件工具，通过此工具开发者可简单快捷的开发TiJOS应用。

### 产品功能

Ti-Dev Studio提供如下功能:

​	创建TiJOS Application工程。

​	支持在线下载tapk应用至设备中。

​	获取并打印设备中输出的日志。

​	支持错误信息快速定位。

​	支持设备管理，快速添加设备至工具中。

​	支持在线安装方式，管理更方便。

# 安装

Ti-Dev Studio支持在线安装和本地安装两种方式来安装插件，开发者可根据实际情况选择一种方式来进行安装即可(推荐使用在线安装)。



### 要求

- Eclipse 4.2 (Juno) or later

- Java 6 or later

  ​

### 在线安装

Ti-Dev Studio可通过Eclipse在线update site地址进行安装。

1. 打开Eclipse点击菜单 Help --> Install New Software... 

![](.\img\20170913175732.png)

1. 在Install窗口中点击Add...，然后在弹出的Add Repository窗口中填入Update Site地址：http://dev.tijos.net/studio/release

![20170913181701](.\img\20170913181701.png)

1. 在界面中选择TiJOS后点击Next 按钮后进入Install Details界面，继续点击Next按钮进入授权页面。在授权界面选择单选按钮I accept the terms of the license agreement后点击Finish进入安装过程。![0170913182250](.\img\20170913182250.png)

![20170913182605](.\img\20170913182605.png)

![20170913182735](.\img\20170913182735.png)



1. 安装结束后弹出提示窗口提示重启Eclipse，点击Yes重启即可。

![20170913183431](.\img\20170913183431.png)

# 卸载

1. 打开Eclipse点击菜单 Help -->点击Installation Details按钮

![20170913201027](.\img\20170913201027.png)

1. 选择Ti-Dev Studio Release后点击Uninstall按钮即可卸载。

![20170913201353](.\img\20170913201353.png)

# 创建工程

### 要求

- Ti-DeviceManager 1.0.17 or later

- TiJOS Runtime 1.0 or later

  ​

通过Ti-Dev Studio创建TiJOS Application工程，过程如下。

1. 打开Eclipse点击菜单 File --> New --> Project...

![20170914093819](.\img\20170914093819.png)

1. 在New Project窗口中选择TiJOS Application Project后点击Next按钮下一步进入工程配置界面

![20170914094054](.\img\20170914094054.png)

1. 在工程配置界面输入工程名并选择TiJOS SDK版本后点击Next按钮下一步进入Settings界面或者Finish按钮完成创建

![20170914094744](.\img\20170914094744.png)

1. 如果进入Settings界面，配置保持默认点击Finish按钮完成创建即可。

   ![20170914095239](.\img\20170914095239.png)

# 调试运行

开发者通过创建TiJOS Application工程进行开发后，可使用调试运行功能来辅助开发。调试运行可在线下载应用至设备中，打印设备输出的日志，解析定位异常信息。



### 链接运行

选择工程右键点击 Run As --> TiJOS Application后将进行代码链接并下载至设备中运行，代码链接将在Console中实时输出链接结果信息。

![20170914111648](.\img\20170914111648.png)

![20170914112324](.\img\20170914112324.png)



### 日志输出

当通过调试运行将TiJOS Application运行至设备中并且返回成功后，Ti-Dev Studio中LogCat View将监听设备串口日志。打开Eclipse点击菜单 Window --> Show View --> TiJOS LogCat 显示日志界面。

![20170914112915](.\img\20170925183001.png)



### 异常定位

代码运行中抛出异常信息并打印在TiJOS LogCat中，可直接在TiJOS LogCat点击异常信息定位至代码具体位置中。

![20170914113234](.\img\20170925183601.png)

如果Console中无法定位至代码中，也可通过点击菜单Ti-Dev --> Exception Query弹出异常查询窗口进行异常查询。在查询窗口中输入相关的错误编码并选择好工程后点击Query查询错误信息，点击Go跳转至具体具体源码位置中。

![20170914113837](.\img\20170914114708.png)

