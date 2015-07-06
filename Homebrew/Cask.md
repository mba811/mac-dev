# Homebrew Cask

你已经感受到了使用 Homebrew 安装命令行程序的便利。那么接下来，我们将通过 Homebrew Cask 优雅、简单、快速的安装和管理 OS X 图形界面程序，比如 Google Chrome 和 Dropbox。

### 安装

安装 Homebrew-cask 是如此的简单直接，运行以下命令即可完成：

    $ brew tap phinze/homebrew-cask
    $ brew install brew-cask
    $ brew cask install google-chrome // 安装 Google 浏览器
    $ brew update && brew upgrade brew-cask && brew cleanup // 更新

### 搜索

如果你想查看 cask 上是否存在你需要的 app，可以到 [caskroom.io](http://caskroom.io/) 进行搜索。

### 文件预览插件

有些 [插件](https://github.com/sindresorhus/quick-look-plugins) 可以让 Mac 上的文件预览更有效，比如语法高亮、markdown 渲染、json 预览等等。

    $ brew cask install qlcolorcode
    $ brew cask install qlstephen
    $ brew cask install qlmarkdown
    $ brew cask install quicklook-json
    $ brew cask install qlprettypatch
    $ brew cask install quicklook-csv
    $ brew cask install betterzipql
    $ brew cask install webp-quicklook
    $ brew cask install suspicious-package

### OS X 图形界面程序

    $ brew cask install alfred
    $ brew cask install appcleaner
    $ brew cask install cheatsheet
    $ brew cask install dropbox
    $ brew cask install google-chrome
    $ brew cask install onepassword
    $ brew cask install sublime-text
    $ brew cask install totalfinder
    ...
---
`译注：`
译者本人并不喜欢 brew cask 的安装方式，更倾向于到 App Store 或官方下载 OS X 图形界面程序。主要因为名字不好记忆、偶尔需要手动更新，另外当你使用 Alfred 或 Spotlight ，你将发现将程序安装在 ~/Application 会很方便。

>Alfred 是个很不错的东西，推荐必须安装。它默认搜索目录不包含brew cask安装的软件，因此手动将`/opt/homebrew-cask`添加到Alfred的搜索目录

### 系统服务管理

  * brew services 命令安装

安装完 homebrew 默认是没有这个命令的，通过 brew services 可以方便地管理通过 homebrew 安装的服务进程，比如 nginx, mysql 等

    brew tap homebrew/services


### Install and start service mysql at login
    
    $ brew install mysql
    $ brew services start mysql
    

Stop service mysql:
    
    $ brew services stop mysql
    

Restart service mysql:
    
    $ brew services restart mysql
    

### [](https://github.com/Homebrew/homebrew-services#install-and-start-dnsmasq-service-at-boot)Install and start dnsmasq service at boot
    
    $ brew install dnsmasq
    $ sudo brew services start dnsmasq


#### SYNOPSIS

# [<sudo>] `brew services` `list`<br>
# [<sudo>] `brew services` `restart` <formula><br>
# [<sudo>] `brew services` `start` <formula> [<plist>]<br>
# [<sudo>] `brew services` `stop` <formula><br>
# [<sudo>] `brew services` `cleanup`<br>

### LaunchRocket — 用于管理 homebrew 安装的服务。可以通过cask来安装。

    brew tap jimbojsb/launchrocket
    brew cask install launchrocket