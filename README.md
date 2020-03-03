# 软硬兼施，实战构建基于AWS IoT的物联网解决方案
## 硬件准备
在这个场景当中，我们将使用到如下的硬件：
*	ESP32开发板：ESP-WROOM-32(ESP32)是乐鑫最新发布的新一代WiFi & 蓝牙双模双核无线通信芯片。芯片集成蓝牙4.2和WiFi HT40技术为一身，拥有高性能Tensilica LX6 双核处理器，支持超低功耗待机，是移动设备、可穿戴电子产品和物联网应用的最佳拍档
![](https://github.com/steelren/aws_iot_core_workshop/blob/master/pics/esp32.jpg)
*	LM35温度传感器：LM35 是由National Semiconductor 所生产的温度传感器，其输出电压为摄氏温标。LM35是一种得到广泛使用的温度传感器。由于它采用内部补偿，所以输出可以从0℃开始。LM35有多种不同封装型式。在常温下，LM35 不需要额外的校准处理即可达到 ±1/4℃的准确率。
![](https://github.com/steelren/aws_iot_core_workshop/blob/master/pics/lm35.jpg) 
    上述硬件通过简单的连接即可组成一个能够通过WIFI网络发送温度数据的温度监测组件。LM35的Vcc，Vout和GND针脚分别对接ESP32的3v3，VP和GND针脚(千万别接错了，否则LM35可烫手了，还有糊味儿☹)。
![](https://github.com/steelren/aws_iot_core_workshop/blob/master/pics/composite.jpg) 
    这样一个组件就可以通过WIFI与AWS IoT Core服务进行连接，实现对温度数据的采集和处理。

## AWS相关服务

