# tijos.framework.sensor.gas - 气体传感类

tijos.framework.sensor.gas中包含了与气体检测、报警相关的类，通过MQ气体检测传感器，测量周围环境中的可燃气体浓度（包含甲烷、丙烷、丁烷、氢气、酒精以及液化气等易燃气体），并通过相应的模拟电压值的输出和数字信号输出实现浓度监测和报警的功能。

包含类如下:

| 类名称  | 说明                                 |
| ---- | ---------------------------------- |
| TiMQ | MQn(n=2/3/4/5/6/7/8/9/135)气体检测传感器类 |



## TiMQ

TiJOS提供使用MQ气体检测传感器的类。

TiJOS MQ 包括如下类：

| 类名                | 说明           |
| ----------------- | ------------ |
| TiMQ              | MQ气体检测传感器类   |
| TiMQEventListener | MQ气体检测报警事件接口 |



## TiMQ的创建、绑定与使用

TiMQ实例在创建时需要和具体总线设备绑定，具体绑定类型与其工作方式以及通讯协议有关，本实例绑定的设备总线类为 tijos.framework.devicecenter.TiGPIO和tijos.framework.devicecenter.TiADC；设备总线的使用请参考：tijos.framework.devicecenter。

构造器如下：

| 构造器                                      | 说明                    |
| ---------------------------------------- | --------------------- |
| TiMQ(TiGPIO gpio, int signalPinID)       | 创建实例                  |
| TiMQ(TiGPIO gpio, int signalPinID, TiADC adc) | 创建实例，允许获取当前传感器输出模拟电压值 |
| TiMQEventListener()                      | 创建实例，气体检测报警事件监听       |

TiMQ类中主要方法的使用：

主要方法如下：

| 方法                        | 说明                  |
| ------------------------- | ------------------- |
| double getAnalogVoltage() | 获取当前传感器输出的电压值（单位：V） |
| long getEventTime()       | 获取事件发生时间，单位：us      |
| int getSignalPinID()      | 获取报警信号pin ID        |




## TiMQ事件监听

TiMQ的事件监听主要通过TiMQEventListener事件回调来处理事件，事件类型包括：

| 方法                                       | 说明      |
| ---------------------------------------- | ------- |
| void setEventListener(TiMQEventListener lc) | 设置监听    |
| void OnAlarm(TiMQ mq)                    | 报警事件    |
| void OnRecovery(TiMQ mq)                 | 传感器恢复事件 |

创建TiMQ事件监听对象：

```java
/*
* 资源使用，
* 创建事件监听对象并设置事件监听
* 在事件监听中处理报警事件逻辑
*/			
MQEventListener lc = new MQEventListener();
mq.setEventListener(lc);
```

事件处理：

```java
class MQEventListener implements TiMQEventListener {
  /*报警事件处理*/
    public void OnAlarm(TiMQ mq){
      /*①读取ADC接口采集到的传感器输出的实际电压值*/
      double vol = mq.getAnalogVoltage();
    }
    /*传感器已恢复到正常状态*/
    public void OnRecovery(TiMQ mq){
    }
}
```

①注：由于MQn类型的传感器本身属于化学成分检测的传感器，对于各类气体的浓度，仅能以电压值的高低来表示。另一方面，化学气体浓度检测传感器在使用前，需要在可信实验室中采用定浓度气体进行对比校准，方可得到传感器的等效的浓度转换曲线以及换算公式。基于以上原因，在我们的示例场景中，并未做xx气体浓度与电压值的换算关系，仅在传感器输出的电压达到较高值（例如5V）时，做出报警的提示，来模拟环境中可燃气体浓度较高、需要报警提示的场景。

TiMQ类中他方法的使用请参考《TiMQ2可燃气体浓度监测例程》。