# 钛极OS(TiJOS)应用开发环境搭建

## 开发平台支持

最低要求：Windows 7及以上

## 安装Eclipse

TiJOS应用与标准Java 应用类似，通过在Eclipse中安装Ti-Dev Studio插件即可通过Eclipse进行TiJOS应用的开发和调试，Eclipse可在http://www.eclipse.org/downloads/ 下载。

如果您已安装Eclipses, 可直接安装Ti-Dev Stuido即可。

Eclipse版本支持：4.6 及以上

## 安装Ti-Dev Manager

TiJOS提供了Ti-Dev Manager安装包，直接点击运行安装程序即可完成。

Ti-Dev Manager安装包可行如下链接获得: [Ti-DevManager_Setup](http://dev.tijos.net/setup/Ti-DeviceManager_setup.exe)

## 安装Ti-Dev Studio Eclipse Plugin

在Eclipse中通过Help菜单下的"Install New Software" 安装Ti-Dev Stuido 插件, 安装过程如下:

1. 从Eclipse菜单"Help"下选择"Install New Software"

   ![TiJOSPlugin_InstallNewSoftware](.\img\TiJOSPlugin_InstallNewSoftware.png)

2. 从弹出的Install对话框中选择"Add"按钮后弹出“Add Repository"后，填写Ti-Dev Studio的插件url http://dev.tijos.net/studio/release 名称任意

   ![TiJOSPlugin_Add](.\img\TiJOSPlugin_Add.png)

   Add Repository

   ![TiJOSPlugin_Location](.\img\TiJOSPlugin_Location.png)

3. 从显示出的"Available Software"中选择"TiJOS"下的"Ti-Dev Studio Release"后， 点击"Next"按钮开始进行安装

   ![TiJOSPlugin_Selection](.\img\TiJOSPlugin_Selection.png)

4. 选择"I accept the terms of the license agreement" 后点击"Finish"即可完成安装

   ![TiJOSPlugin_AcceptLicense](.\img\TiJOSPlugin_AcceptLicense.png)

Installing...

   ![TiJOSPlugin_InstallSoftware](.\img\TiJOSPlugin_InstallSoftware.png)



5. 安装完成后重新启动Eclipse之后，在Eclipse的菜单中增加"Ti-Dev"

   ![TiJOSPlugin_Ti-Dev](.\img\TiJOSPlugin_Ti-Dev.png)

在新建工程时选择“Other” 时， 即可看到TiJOS Application Project的选项

   ![TiJOSPlugin_Project](.\img\TiJOSPlugin_Project.png)

当新建TiJOS Application Project后， 完成编码在TiKit开发板上进行测试时， 可选择"Run As  TiJOS Application" 在开发板上运行

   ![TiJOSPlugin_RunAs](.\img\TiJOSPlugin_RunAs.png)



经过以上步骤后， Ti-Dev Studio 即成功安装并运行在Eclipse当中。

## 连接TiKit开发板

将TiKit硬件开发板连接到开发机器， 并在Ti-Dev Manager添加设备，检测设备连接，如果是网络应用，还可在Ti-Dev Manager中配置网络设置，如无线WIFI， 网关，DNS等等， 在进行配置时， 请将开发板设置为BOOT模式， 在开发过程中可根据需求连接相关的传感器进行开发和测试。

## TiJOS应用开发

完成以上设置后， 通过Eclipse中新建TiJOS Application Project即可进行TiJOS应用开发了。 