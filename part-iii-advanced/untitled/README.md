# 应用调试

应用调试是ThingsCloud平台给开发用户提供的一个便捷实用的功能，通过应用调试，应用开发者可以非常方便的调试远程边缘计算网关中运行的代码，通过在线的WEBIDE，可以非常方便的编写应用代码并下载到远程的边缘计算网关，查看代码执行的输出结果。而在线的WEBIDE，也对FreeIOE应用开发的LUA编程语言支持非常良好，提供语法高亮，代码提示，错误提示等功能。

在ThingsCloud平台上开启应用调试有如下要求：
1. 首先需要在ThingsCloud平台上注册账户并申请为开发者角色。
2. 账户名下有内置了FreeIOE的边缘计算网关，或者运行了FreeIOE的虚拟网关。
3. 远程调试的网关必须通过网关的高级设置开启网关的调试模式。
4. 在目标网关在安装应用，然后通过应用的管理工具条点击应用调试。


网关开启调试模式请参考 [3.1 网关高级设置](part-iii-advanced/untitled-1.md)

当以上条件均满足时，在目前网关的应用列表中选中欲进行应用调试的应用，点击工具栏上的应用调试按钮，即进入到应用的远程调试，如下图所示：
![](../../v1/part-iii\ThingsCloud_2019-06-27_13-31-13.png)

点击“应用调试”按钮，系统会检查当前用户和应用开发者是否是相同用户，如是相同用户，则会直接进入代码编辑页面；如不是相同用户，则弹出提示窗口，提示需要将应用开发者的应用克隆到当前用户名下才能进行应用调试，如下图所示：
![](../../v1\part-iii\ThingsCloud_2019-06-24_13-24-45.png)

进入代码编辑器的页面,我们可看到页面的主视图由网关状态栏，代码编辑器工具栏，左侧文件树导航，右侧代码编辑区组成。如下图所示:
![](../../v1\part-iii\ThingsCloud_2019-06-24_13-26-13.png)

通过左侧文件树导航我们切换到app.lua，就可看到应用的核心代码了，如下图所示：
![](../../v1\part-iii\ThingsCloud_2019-06-24_13-26-14.png)

代码编辑器工具栏，主要分为文件树操作图标和代码功能图标2部分，代码功能图标主要提供了1）代码上传保存图标；2）字体放大图标；3）字体缩小图标；4）版本发布图标；5）版本回滚图标；6）打包下载到网关图标。如下图所示：
![](../../v1\part-iii\ThingsCloud_2019-06-24_13-26-27.png)

通过代码上传保存图标，我们可以将当前应用在代码编辑器中的代码上传保存到服务器上的代码缓存区，后期可在任何时间或任何地方接着目前的进度进行代码编辑，通过代码编辑提供了大量的快捷键操作命令，如CTRL+S——快速保存代码，CTRL+F——在代码中查找关键词，CTRL+H——在代码中查找并替换，等等快捷键。如下图所示：
![](../../v1\part-iii\ThingsCloud_2019-06-24_13-27-03.png)

发布新版本图标可将当前编辑的代码保存并生成一个新的版本（测试版）保存到应用服务器中，如下图所示：
![](../../v1\part-iii\ThingsCloud_2019-06-24_13-27-22.png)

在弹出的窗口中输入新的版本号以及更新日志，点击确认按钮即可，如版本号已经存在，则更新不成功，如下图所示：
![](../../v1\part-iii\ThingsCloud_2019-06-24_13-27-30.png)

版本回滚图标提供了将应用代码回退到原来的某个版本的功能，如下图所示：
![](../../v1\part-iii\ThingsCloud_2019-06-24_13-27-42.png)


在弹出的窗口中由当前应用在服务器存储的版本列表，选择欲回退的版本即刻，如下图所示：
![](../../v1\part-iii\ThingsCloud_2019-06-24_13-27-57.png)

而安装当前代码到网关可将目前正在编写的应用代码打包下载到当前操作的网关中并将代码运行起来。如下图所示：
![](../../v1\part-iii\ThingsCloud_2019-06-24_13-28-09.png)
如代码下载到目标网关成功，则会提示下载成功，如下图所示：
![](../../v1\part-iii\ThingsCloud_2019-06-24_13-28-21.png)

应用代码下载到远程网关，作为开发者来说，是很关心应用是否能正常运行？功能是否正常？程序的输入日志如何查看？程序和设备通讯的报文如何查看？这些功能请看接下来的章节。
[3.4 网关日志](wang-guan-ri-zhi.md)
[3.5 通讯报文](tong-xun-bao-wen.md)


