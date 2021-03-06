# 网关调试模式

内置了FreeIOE的边缘计算网关默认状态是非调试模式，在非调试模式下，有如下限制：

1. 只能升级正式发行版的固件升级包。
2. 只能安装正式发行版的应用程序。
3. 不能在freeioe中创建本地应用。
4. 不能在freeioe中修改已经安装的应用。
5. 不能在平台上修改远程freeioe中的应用。

作为应用开发者，是需要将freeioe置为调试模式以便于开发调试freeioe的应用。

**开启freeioe的调试模式的方式如下:**

登录平台后，选择目标网关（ThingsLink或者内置freeioe的网关），在网关设置页面中，点击高级设置按钮，在高级设置的面板中点击“调试模式”后的开关按钮，稍候片刻，即可收到目标设备已开启调试模式的通知。开启成功后在网关的状态栏中会出现调试模式开启的标记，如下图所示：
![](../v1\part-ii\ThingsCloud_2019-06-26_18-13-01.png)