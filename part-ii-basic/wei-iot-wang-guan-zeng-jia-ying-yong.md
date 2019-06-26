# 为IOT网关增加应用

未使用过的网关是不带任何应用的，也就是说，你如果在网关列表在点击网关后面的“设备按钮”，“应用”按钮，进入网关数据或应用，那么将看不到任何应用功能，也看不到任何外部设备，只能看见网关自身（包含了网关自身的一些系统变量），如想要网关具有你需要的功能，那么需要从应用商店安装满足你需求的应用。
进入一个新网关的界面：
 ![](..\v1\part-ii\ThingsCloud_2019-06-24_12-15-23.png)
展开ThingsLink，可以看见网关自身的变量数据
 ![](..\v1\part-ii\ThingsCloud_2019-06-24_12-15-47.png)

切换到应用列表，应用列表为空。
 ![](..\v1\part-ii\ThingsCloud_2019-06-24_12-27-00.png)

下面是给网关增加应用的步骤：

1. 进入“网关应用”页面后，提示未安装任何应用，点击“安装应用”按钮，如下图所示：  
    ![](..\v1\part-ii\ThingsCloud_2019-06-24_12-27-17.png) 

2. 列出目前平台公开可以访问的应用，如下图所示：   
![](..\v1\part-ii\ThingsCloud_2019-06-24_12-27-32.png)

3. 通过搜索功能，将应用范围缩小，如下图所示： 
![](..\v1\part-ii\ThingsCloud_2019-06-24_12-27-49.png)
 
4. 点击应用图标，查看应用的介绍及其他信息，如下图所示：
![](..\v1\part-ii\ThingsCloud_2019-06-24_12-27-59.png)

接下来，以ModbusTCP模拟设备和西门子PLC S7-1200为例说明ThingsCLoud平台如何给ThingsLink安装应用。
* [举例1：采集Modbus 仿真数据](part-ii-basic/tong-guo-iot-ying-yong-cai-ji-she-bei-shu-ju.md)
* [举例2：采集PLC S7-1200数据](part-ii-basic/tong-guo-iot-ying-yong-cai-ji-she-bei-shu-ju-2.md)