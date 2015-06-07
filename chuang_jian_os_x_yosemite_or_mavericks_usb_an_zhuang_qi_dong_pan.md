# 创建 OS X Yosemite or Mavericks USB 安装启动盘

> **Update - 2014年10月17日 OS X Yosemite正式版发布，仍然可以使用此方法创建 USB 启动盘** OS X Yosemite正式版发布，仍然可以使用此方法创建 USB 启动盘，你只需要将「Install OS X Mavericks.app」换成「Install OS X Yosemite.app」就可以了。

之前的Mac OS X安装盘创建都是通过`Disk Utility`里的Restore还原`InstallESD.dmg`到U盘来制作的，从 App Store 下载的正式版 OS X Mavericks 安装包里，提供了一个更简单的工具 `createinstallmedia` 帮我们更容易的创建USB安装启动盘。

## 第1步. 从App Store下载 OS X Mavericks（如果已经下载好，跳过此步）

第1步很简单，下载OS X Mavericks，不多说了。

![从App Store下载 OS X Mavericks](http://ksmx.me/content/images/2013/10/download-mavericks-app-store.png)

> 经过[little_cup](http://www.v2ex.com/member/little_cup)的补充，只有InstallESD.dmg是可行的，更名为InstallESD.dmg.pkg，双击安装，之后就会在「应用程序」里生成Install OS X Mavericks.app

## 第2步. 在安装界面的第一个页面停下

从App Store完成下载后，OS X Mavericks安装程序会自动启动，不要点击继续，停在**安装界面第一页**，如下图：

![OS X Mavericks安装界面第一页](http://ksmx.me/content/images/2013/10/first-screen-of-mavericks-installation.png)

> 如果你的 `Install OS X Mavericks.app` 不是通过App Store下载的，你可以双击下载回来的文件打开。

## 第3步. 格式化U盘

U盘最少需要8G，上面的资料备份好，创建启动盘会抹掉整个U盘。执行下面的步骤：

  1. 插入U盘
  2. 启动 `Disk Utility`
  3. 在左边的硬盘选择中，点击选中你的U盘
  4. 然后在右边，选择 「Partition」
  5. 「Partition Layout」下的下拉框中，选择1个分区
  6. （可选）点击 「Options..」，选中 「GUID Partition Table」，一般来说这个是默认的，可以检查一下
  7. 点击 「Apply」

![格式化U盘](http://ksmx.me/content/images/2013/10/disk-utility-partition.png)

> 如果不希望完全格式化，你可以只格式化一个分区

## 第4步. 执行创建USB安装启动盘的命令

打开 `Terminal`，运行下面的命令：
	
	sudo /Applications/Install\ OS\ X\ Mavericks.app/Contents/Resources/createinstallmedia --volume /Volumes/Untitled\ 1 --applicationpath /Applications/Install\ OS\ X\ Mavericks.app --nointeraction
	
	# 这里简单解释一下，命令分为5个部分
	#
	# 1. sudo #以root权限执行命令
	# 2. /Applications/Install\ OS\ X\ Mavericks.app/Contents/Resources/createinstallmedia #也就是我们要运行的程序
	# 3. --volume /Volumes/Untitled\ 1 #是指定我们U盘分区的位置
	# 4. --applicationpath /Applications/Install\ OS\ X\ Mavericks.app #是指定OS X安装包的位置
	# 5. --nointeraction #以非交互式的方式运行，这样就不会不停的问Yes/No了
	

那么一大串命令简化后是：

`sudo $命令位置 --volume $U盘的路径 --applicationpath $安装包路径 --nointeraction`

里面需要3个参数都是路径，如果你是自己下载的 `Install OS X Mavericks.app` 没有放在 `/Applications`下，以上的3个路径位置需要稍作修改（例如 `Install OS X Mavericks.app` 是放在 Downloads目录，前缀是 ~/Downloads）。**建议将`Install OS X Mavericks.app`移动到`/Applications`下，这样直接可以复制上面的运行。**

指令成功运行后，你会看到下图的界面：

![createinstallmedia命令运行](http://ksmx.me/content/images/2013/10/createinstallmedia-command.png)

等待创建完成后，你的U盘就变成了这样：

![OS X Mavericks USB安装启动盘](http://ksmx.me/content/images/2013/10/os-x-mavericks-usb-installer.png)

重启系统，一直按着键盘上的「Option」按键，就可以进行全新安装。

> **Update - 2014年4月6日** 安装进度会卡在`About a second remaining`很长时间，这个是正常的，不用担心，多等几分钟就可以了。