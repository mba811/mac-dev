# Sublime Text

Sublime Text 是一款跨平台代码编辑器（Not IDE），拥有非常丰富成熟的插件，辅以大量的快捷键，足使开发效率成倍提升。

另外，GitHub 在去年开源了一款叫 [Atom](https://atom.io/) 的代码编辑器，基本和 Sublime Text 无异。不过是基于 Node.js 和 Chromium，这个会在下面进行介绍。Atom 也是我目前的主力编辑器。

### 安装

目前最新版本为 Sublime Text 3，在[官方网站](http://www.sublimetext.com/3)提供了各个平台的下载。推荐使用此版本，有部分插件只支持 Sublime Text 3。

下载装完之后。打开iTerm2，设置subl命令，使得能够在shell中，直接通过subl命令调用。设置软链接如下：

    $ ln -s /Applications/Sublime\ Text.app/Contents/SharedSupport/bin/subl /usr/local/bin/subl
