# MacPorts 使用

MacPorts官方网站[http://www.macports.org](http://www.macports.org/)  
  
更新ports tree和MacPorts版本，强烈推荐第一次运行的时候使用-v参数，显示详细的更新过程。

    sudo port -v selfupdate  
  
搜索索引中的软件

    port search name  
  
安装新软件

    sudo port install name  
  
卸载软件

    sudo port uninstall name  
  
查看有更新的软件以及版本

    port outdated  
  
升级可以更新的软件

    sudo port upgrade outdated  
  
Eclipse的插件需要subclipse需要JavaHL，下面通过MacPorts来安装

    sudo port install subversion-javahlbindings
