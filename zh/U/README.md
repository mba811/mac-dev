# 制作 Yosemite 安装 U 盘

Yosemite 正式发布了，已经可以通过 App Store 下载，不过在下载完5.17GB 的安装包以后不忙急着安装，可以先制作一个 Yosemite 的安装 U盘，因为安装包在更新完系统以后会被自动删除。

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/m-u/u1.png)

应用程序 - Yosemite 安装包

准备一个8GB 的 U盘，用「应用程序 - 实用工具 - 磁盘工具」格式化成「Mac OS X 扩展（日志式）」格式，并将盘符命名为「Untitled」，盘符名称和下面的命令行是对应的，如果你使用其他盘符名称需要对应修改命令行中的盘符名称。

打开「应用程序 - 实用工具 - 终端」，复制粘贴输入以下命令：

> `sudo /Applications/Install\ OS\ X\ Yosemite.app/Contents/Resources/createinstallmedia --volume /Volumes/Untitled --applicationpath /Applications/Install\ OS\ X\ Yosemite.app --nointeraction`

执行命令前会提示你输入账户密码，密码不会显示，输入完成后直接 return即可。

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/m-u/u2.png)


接下来耐心等待，直到「终端」程序界面中提示已经「Done」完成制作。

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/m-u/u3.png)

如果你觉得命令行的方式有点麻烦，还有一个途径就是下载专门制作安装 U盘的[Diskmakerx](http://diskmakerx.com/) 工具，安装后用它来制作，当然前提也是你的 Yosemite 安装包已经下载好了。

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/m-u/u4.png)

* * *

使用 U盘引导机器的方法：重启机器出现灰白色的苹果界面，听到「当」的一声后按下「option」键就进入了引导设备的选择界面，将指针移动到黄色的 U盘选择启动即可。

![](http://7q5cfr.com1.z0.glb.clouddn.com/@/m-u/u5.png)


