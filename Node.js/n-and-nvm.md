Node版本的迭代速度很快，版本很多（横跨0.6到0.11），升级Node版本成为了一个问题。目前有`n`和`nvm`这两个工具可以对Node进行无痛升级，本文简单介绍一下二者的使用。

# n

`n`是Node的一个模块，作者是[TJ Holowaychuk](https://github.com/visionmedia)（鼎鼎大名的[Express](http://expressjs.com/)框架作者），就像它的名字一样，它的理念就是简单：
    
    "no subshells, no profile setup, no convoluted api, just simple"
    

安装很简单：
    
    $ sudo npm install -g n
    

安装完成之后，直接输入`n`后输出当前已经安装的node版本以及正在使用的版本（前面有一个`o`），你可以通过移动上下方向键来选择要使用的版本，最后按回车生效。
    
    $ n
        0.10.1 
        0.10.15 
    o   0.10.21 
        0.11.8
    

如果你要安装其他的版本（比如0.11.12），那么如下：
    
    $ n 0.11.12
    install : 0.11.12
       mkdir : /usr/local/n/versions/0.11.12
       fetch : http://nodejs.org/dist/v0.11.12/node-v0.11.12-darwin-x64.tar.gz
    ####                                                     5.9%
    

安装最新的版本
    
    $ n latest
    

安装稳定版本
    
    $ n stable
    

删除某个版本
    
    $ n rm 0.10.1 
    

以指定的版本来执行脚本
    
    $ n use 0.10.21 some.js
    

# nvm

[nvm](https://github.com/creationix/nvm)全称Node Version Manager，它与`n`的实现方式不同，其是通过shell脚本实现的。

安装方式有两种：
    
    $ curl https://raw.github.com/creationix/nvm/v0.4.0/install.sh | sh
    

或者
    
    $ wget -qO- https://raw.github.com/creationix/nvm/v0.4.0/install.sh | sh
    

以上脚本会把`nvm`库clone到`~/.nvm`，然后会在`~/.bash_profile`, `~/.zshrc`或``~/.profile`末尾添加source，安装完成之后，你可以用以下命令来安装node
    
    $ nvm install 0.10
    

使用指定的版本
    
    $ nvm use 0.10
    

查看当前已经安装的版本
    
    $ nvm ls
    .nvm
    ->  v0.10.24
    

查看正在使用的版本
    
    $ nvm current
    v0.10.24
    

以指定版本执行脚本
    
    $ nvm run 0.10.24 myApp.js
    

卸载nvm
    
    $ rm -rf ~/.nvm
    

# 总结

以上就是两种Node版本管理工具的安装和基本使用方法，选择适合你的那一种口味。

# 参考

  * [https://github.com/creationix/nvm](https://github.com/creationix/nvm)
  * [https://github.com/visionmedia/n](https://github.com/visionmedia/n)
