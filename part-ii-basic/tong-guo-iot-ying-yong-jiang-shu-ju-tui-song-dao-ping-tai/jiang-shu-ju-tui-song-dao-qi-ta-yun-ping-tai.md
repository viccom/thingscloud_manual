# 将数据推送到其他云平台

如要将freeioe在应用采集到设备数据推送到指定的平台，需要在freeioe中安装指定的应用，一般来说，此应用都是针对指定的平台进行开发的。由于此类应用设计到平台自身的通讯协议及数据格式，因此，多是专用的应用。

本节内容以将网关的数据（可通过应用程序过滤）推送到自建MQTT服务器为例进行说明。

1) 自建MQTT Broker实际很简单，首先有一台互联网上可以访问的主机就可，这里我使用一台阿里云的ECS作为MQTT Broker服务器，然后再找一个MQTT Broker软件即可，由于目前大多数物联网的平台都采用MQTT协议作为平台接入协议，因此各种MQTT Broker软件非常多，商业版本/免费版本/开源版本都有很多的选择，下面就是一张关于各种mqtt broker功能对比的图片：
   ![](../../v1\part-ii\ThingsCloud_emq.png)
   上图中的信息来自 [https://github.com/mqtt/mqtt.github.io/wiki/server-support](https://github.com/mqtt/mqtt.github.io/wiki/server-support)
   在本例中，我们采用国产的MQTT Broker [EMQ X Broker](https://www.emqx.io/cn/downloads#broker)，EMQ X Broker支持主流的各种操作系统Linux/Mac OS/Windows，这里我们选择Ubuntu/Linux版本，[按照官方安装指南](https://developer.emqx.io/docs/broker/v3/cn/install.html#ubuntu)非常容易的就将EMQ X Broker安装并运行起来了。EMQ X Broker自带WEB管理端，

2) 更改防火墙安全规则，开启MQTT Broker服务器的TCP端口，由于本例中使用了阿里云的ECS主机，默认情况下，MQTT Broker的服务端口并未在ECS主机的外部防火墙规则中开启，因此需要登录阿里云账户，在ECS主机的安全规则中开启MQTT Broker的服务端口，一般开启TCP端口1883，8883即可；如需要远程管理EMQ X Broker，可开启TCP端口18083；如前端页面需要直接访问EMQ X Broker，开启TCP端口8083，8084；更加详细的说明，可阅读EMQ X Broker的帮助文档。

3) 上面2步完成后，可通过mqtt客户端工具测试一下EMQ X Broker工作是否正常，这里使用网上使用者较多的mqtt客户端工具[mqttfx](http://mqttfx.jensd.de/index.php/download),通过此客户端工具，能和自己部署的MQTT Broker收发消息，就说明工作正常了。下面继续说明如何在ThingsCloud平台配置ThingsLink网关，将ThingsLink网关的数据推送到自建的MQTT Broker。
   
4) 在ThingsCloud平台上选择目标网关进入应用列表，点击右上角的“安装新应用”，搜索名称为"mqtt_demo"的应用，点击安装图标，进入安装配置界面，如下图所示：
   
5) 搜索