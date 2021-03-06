# 浏览采集的数据

ThingsCLoud平台作为边缘计算（FreeIOE）网关的管理运维平台，提供了对采集应用基本的数据浏览查询功能，通过ThingsCLoud提供的数据浏览功能，我们可以在平台上查看应用采集到的实时数据或内部变量，也可以通过平台对设备做数据下置，发送控制指令等操作。

在目标网关的配置管理界面中，点击“设备列表”，就可查看网关采集设备数据的情况。


1) 进入目标网关的管理界面，切换到“设备列表”，可以看见我们上节中添加的2个仿真设备，加上ThingsLink网关自身的系统变量，一共有3个设备，如下图所示：

![](..\v1\part-ii\ThingsCloud_2019-06-25_09-58-15.png)

2) 点击某个设备(如dev1设备)，可进入设备实时数据浏览页面。如下图所示：

![](..\v1\part-ii\ThingsCloud_2019-06-24_13-04-25.png)

3) 在在界面中，我们可看到dev1设备的实时数据，此页面的数据默认是自动实时刷新的(周期1秒)。由于网关默认是未开启向ThingsCloud上送数据，因此列表中的数据都是空，如下图所示：
![](..\v1\part-ii\ThingsCloud_2019-06-24_13-04-25.png)
    如网关未开启向ThingsCloud平台推送数据，在页面的左上角会有图标提示，第一个图标是网关在线状态的图标，第2个图标就是网关是否开启数据上送的图标（当前是未开启）。
![](..\v1\part-ii\ThingsCloud_2019-06-24_13-04-47.png)

4) 如网关未开启向ThingsCloud上送数据，点击“开启临时数据上送”按钮后，网关会在周期（网关上送周期）的将网关的变化数据上传到ThingsCloud平台，再次点击此按钮，网关会在60秒后停止上送数据。当此页面跳转或关闭后，网关也会在60秒后停止上送数据。开始数据上送后可以看见采集的实时数据，如下图所示：
   ![](..\v1\part-ii\ThingsCloud_2019-06-25_10-18-18.png)

5) 点击数据右侧的“数据浏览”，可查询当前数据点存储在ThingsCloud平台的历史数据（最近10分钟）。如下图所示：
   ![](..\v1\part-ii\ThingsCloud_2019-06-25_10-25-21.png)   

6) 切换到“数据下置”列表，可以对网关应用采集的设备进行数据下写的功能。由于dev1中未配置数据下置点，切换到d1设备，可数据下置的标签是q0_0,通过这个标签也是可读取的，当前数值是1，如下图所示：
   ![](..\v1\part-ii\ThingsCloud_2019-06-25_10-26-45.png)
   在数据下置列表中通过下置按钮对标签q0_0写入数据0，很快就收到网关执行的反馈结果，同时数据浏览列表中的标签q0_0的实时数据已经改为为0了
   ![](..\v1\part-ii\ThingsCloud_2019-06-25_10-27-16.png)

7) 切换到“控制指令”列表，可以对网关应用采集的设备下发控制指令的功能。

