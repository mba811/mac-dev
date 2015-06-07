# 通用开发环境设置

##编译环境Xcode

Xcode: 在App Store里面免费下载。Apple官方出品。编译下软件与开发mac、ios等软件需要。安装好Xcode之后，打开偏好设置，安装command line，如下图所示：

![Commandtool 2013](http://www.yangzhiping.com/images/mac-2013-dev/commandtool-2013.png)

特别提醒：

Mac 10.9之后，安装command line的方式略有变化，请参考：

  * [OS X 10.9 Mavericks下如何安装Command Line Tools(命令行工具) - Licess's Blog](http://blog.licess.org/how-to-install-command-line-tools-in-osx-10-9-mavericks/)

## 终端iTerm2

终端:[iterm2](http://www.iterm2.com/)：下载地址是：[https://code.google.com/p/iterm2/downloads/list](https://code.google.com/p/iterm2/downloads/list)

更多技巧参考老文：[iTerm2新手应知特色功能](http://www.yangzhiping.com/tech/iterm2.html)。比如，可以查询出所有之前的命令历史：

![iterm2 Paste History](http://www.yangzhiping.com/images/first-ruby/iterm2-paste-history.png)

## 编辑器subl

[sublimetext](http://www.sublimetext.com/)日益流行，下载装完之后。打开iTerm2，设置subl命令，使得能够在shell中，直接通过subl命令调用。设置软链接如下：
    
    sudo ln -s "/Applications/Sublime Text 2.app/Contents/SharedSupport/bin/subl" /usr/bin/subl
    

这一步骤容易出错，请在iterm2中，打印当前`PATH`，看系统默认的查找路径次序是多少。命令是：
    
    $PATH
    

如果系统默认查找的是/bin在前（要搞得多乱的系统。。。），请将软链接指向的`/usr/bin/subl`更改为`/bin/subl`。

进一步的设置与插件安装，参考：

  * [Sublime Text 3 for Python development · Piotr Banaszkiewicz](http://piotr.banaszkiewicz.org/blog/2013/08/24/sublime-text-3-for-python-development/)
  * [Sublime Text 2 for Ruby](http://blog.codeclimate.com/blog/2012/06/21/sublime-text-2-for-ruby/)
  * [Sublime Text 資源整理](http://ihower.tw/blog/archives/7375)

另一个Mac极其流行的编辑器是TextMate，开源版[下载地址](http://macromates.com/download)

关于它的使用，敬请参考我的老文章。或者：

  * 图书：[Textmate: Power Editing for the Mac](http://book.douban.com/subject/1908201/)
  * [Using Textmate as your default editor](https://help.github.com/articles/using-textmate-as-your-default-editor)

## 安装homebrew

brew是mac下级别的，用于安装一切Mac需要但没提供的软件。比如mysql等。打开iTerm2，输入：
    
    ruby -e "$(curl -fsSL https://raw.github.com/mxcl/homebrew/go)"
    

如果担心找不到Ruby、CURL等所在地，可以使用以下替代命令：
    
    /usr/bin/ruby -e "$(/usr/bin/curl -fksSL https://raw.github.com/mxcl/homebrew/master/Library/Contributions/install_homebrew.rb)"
    

安装wget等通用软件
    
    brew install wget
    brew install curl
    brew install openssl
    brew install imagemagick #未来Rails图片处理需要
    brew install gfortran #未来R语言等编译需要
    brew install node #未来安装Ruby web服务器pow需要
    

需要使得系统默认识别的路径，优先识别brew所在的。方法就是编辑：/etc/paths。调用subl打开：
    
    subl /etc/paths
    

使得它的次序先后是：
    
    /usr/local/bin
    /usr/bin
    /bin
    /usr/sbin
    /sbin
    

brew安装的与系统自带的同类软件有什么区别呢？它始终是从github下载最新的。

## 下载.dotfiles

dotfiles是很多程序员，将自己的配置环境放在网上。使得未来避免很多重复工作。一般建议找一个与自己类似的。笔者参考zan5hin的修改。
    
    cd ~/. #进入根目录
    git clone https://github.com/zanshin/dotfiles.git ~/.dotfiles
    cd ~/.dotfiles
    git submodule init 
    git submodule update 
    

请注意，dotfiles下载之后，我们这个时候还没下载zsh、oh-myzsh等等，所以，此时先不执行配置文件中的内容。等下载完它们了，再来执行。

## 安装zsh与oh-my-zsh
    
    brew install zsh
    

[oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh)是一个流行的zsh配置文件包。
    
    cd ~/.  #进入根目录
    #自动安装脚本    
    wget --no-check-certificate https://github.com/robbyrussell/oh-my-zsh/raw/master/tools/install.sh -O - | sh
    

使用之前`git clone`下来的`.dotnetfiles`来管理zsh等很多配置文件。创建软链接，使得ZSH等配置文件默认由它来管理：
    
    ln -s ~/.dotfiles/zsh ~/.zsh
    ln -s ~/.dotfiles/zsh/zshrc ~/.zshrc
    ln -s ~/.dotfiles/zsh/zshenv ~/.zshenv
    ln -s ~/.dotfiles/zsh/zprofile ~/.zprofile
    

如果提示：`ln: /Users/psytown/.zshrc: File exists`，请删除该文件，命令为：
    
    rm -rf ~/.zshrc  #请注意，将psytown更改为你的Mac的用户名
    

设置zsh为默认shell
    
    subl /etc/shells
    

在文末增加：
    
    /usr/local/bin/zsh
    

将zsh设置为默认的Shell：
    
    chsh -s /usr/local/bin/zsh
    

重新启动iterm2。

更详细的参考老文：

  * [zsh与oh-my-zsh](http://www.yangzhiping.com/tech/zsh-oh-my-zsh.html)