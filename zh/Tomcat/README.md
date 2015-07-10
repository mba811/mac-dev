# 通过 Homebrew 安装 Tomcat

    brew install tomcat 

## 安装Tomcat

在Apache网站下载最新的Tomcat二进制编码包：http://tomcat.apache.org/ （注意别下载了Windows的安装包） 下载完后，解压，并将文件夹命名为Tomcat 将重命名的文件夹移动到根目录/Volumes/Data/sdk/中（别处也可），安装过程便完成了

执行/Volumes/Data/sdk/tomcat7/bin下的startup.sh，然后打开http://localhost:8080查看是否Tomcat已经启动，若要停止服务器就运行同目录下的shutdown.sh

如果遇到诸如无法找到目录以及文件地问题，一般是因为文件权限造成地问题，可以如此解决：

    sudo chmod 755 /Volumes/Data/sdk/tomcat7/*.sh

**Tips**

遇见”JAVA_HOME not defined”JAVA路径未定义错误，在终端中执行以下命令：

    sudo setenv JAVA_HOME /Library/Java/Home

## 配置Tomcat启动脚本

使用文本编辑器添加以下代码：

```
#!/bin/bash
 
export TOMCAT_HOME="/Volumes/Data/sdk/tomcat7"
 
case $1 in
start)
sh $TOMCAT_HOME/bin/startup.sh
;;
stop)
sh $TOMCAT_HOME/bin/shutdown.sh
;;
restart)
sh $TOMCAT_HOME/bin/shutdown.sh
sh $TOMCAT_HOME/bin/startup.sh
;;
*)
echo "Usage: start|stop|restart"
;;
esac
 
exit 0
```

将文件保存为tomcat，小写并不带后缀。将这个文件放置到终端包含的路径中，例如/usr/bin，而后便可以在终端中简单地输入tomcat start和tomcat stop启用tomcat了。
