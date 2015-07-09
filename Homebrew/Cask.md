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

# Quick Look plugins

> List of useful [Quick Look](http://en.wikipedia.org/wiki/Quick_Look) plugins for developers

## [](https://github.com/sindresorhus/quick-look-plugins#install)Install

### [](https://github.com/sindresorhus/quick-look-plugins#using-homebrew-cask)Using [Homebrew Cask](https://github.com/phinze/homebrew-cask)

  * Run `brew cask install <package>`

#### [](https://github.com/sindresorhus/quick-look-plugins#install-all)Install all
    
    brew cask install qlcolorcode qlstephen qlmarkdown quicklook-json qlprettypatch quicklook-csv betterzipql qlimagesize webpquicklook suspicious-package
    

### [](https://github.com/sindresorhus/quick-look-plugins#manually)Manually

  * Click "download manually"
  * Move the downloaded .qlgenerator file to /Library/QuickLook
  * Run `qlmanage -r`

## [](https://github.com/sindresorhus/quick-look-plugins#plugins)Plugins

### [](https://github.com/sindresorhus/quick-look-plugins#qlcolorcode)[QLColorCode](https://code.google.com/p/qlcolorcode/)

> Preview source code files with syntax highlighting

Run `brew cask install qlcolorcode` or [download manually](https://qlcolorcode.googlecode.com/files/QLColorCode-2.0.2.tgz)

![](http://7q5cfr.com1.z0.glb.clouddn.com/QLColorCode.png)

### [](https://github.com/sindresorhus/quick-look-plugins#qlstephen)[QLStephen](https://github.com/whomwah/qlstephen)

> Preview plain text files without a file extension. Example: README, CHANGELOG, etc.

Run `brew cask install qlstephen` or [download manually](https://github.com/whomwah/qlstephen/releases)

![](http://7q5cfr.com1.z0.glb.clouddn.com/QLStephen.png)

### [](https://github.com/sindresorhus/quick-look-plugins#qlmarkdown)[QLMarkdown](https://github.com/toland/qlmarkdown)

> Preview Markdown files

Run `brew cask install qlmarkdown` or [download manually](https://github.com/downloads/toland/qlmarkdown/QLMarkdown-1.3.zip)

![](http://7q5cfr.com1.z0.glb.clouddn.com/QLMarkdown.png)

### [](https://github.com/sindresorhus/quick-look-plugins#quicklookjson)[QuickLookJSON](http://www.sagtau.com/quicklookjson.html)

> Preview JSON files

Run `brew cask install quicklook-json` or [download manually](http://www.sagtau.com/media/QuickLookJSON.qlgenerator.zip)

![](http://7q5cfr.com1.z0.glb.clouddn.com/QuickLookJSON.png)

### [](https://github.com/sindresorhus/quick-look-plugins#qlprettypatch)[QLPrettyPatch](https://github.com/atnan/QLPrettyPatch)

> Preview .patch files

Run `brew cask install qlprettypatch` or [download manually](https://github.com/atnan/QLPrettyPatch/releases)

![](http://7q5cfr.com1.z0.glb.clouddn.com/QLPrettyPatch.png)

### [](https://github.com/sindresorhus/quick-look-plugins#quicklookcsv)[QuickLookCSV](https://github.com/p2/quicklook-csv)

> Preview CSV files

Run `brew cask install quicklook-csv` or [download manually](http://quicklook-csv.googlecode.com/files/QuickLookCSV.dmg)

![](http://7q5cfr.com1.z0.glb.clouddn.com/QuickLookCSV.png)

### [](https://github.com/sindresorhus/quick-look-plugins#betterzipql)[BetterZipQL](http://macitbetter.com/BetterZip-Quick-Look-Generator/)

> Preview archives

Run `brew cask install betterzipql` or [download manually](http://macitbetter.com/BetterZipQL.zip)

![](http://7q5cfr.com1.z0.glb.clouddn.com/BetterZipQL.png)

### [](https://github.com/sindresorhus/quick-look-plugins#qlimagesize)[qlImageSize](https://github.com/Nyx0uf/qlImageSize)

> Display image size and resolution

Run `brew cask install qlimagesize` or [download manually](https://github.com/Nyx0uf/qlImageSize#installation)

![](http://7q5cfr.com1.z0.glb.clouddn.com/qlImageSize.png)

### [](https://github.com/sindresorhus/quick-look-plugins#webp)[WebP](https://github.com/dchest/webp-quicklook)

> Preview WebP images

Run `brew cask install webpquicklook` or [download manually](https://github.com/dchest/webp-quicklook/releases)

![](http://7q5cfr.com1.z0.glb.clouddn.com/WebP.png)

### [](https://github.com/sindresorhus/quick-look-plugins#suspicious-package)[Suspicious Package](http://www.mothersruin.com/software/SuspiciousPackage/)

> Preview the contents of a standard Apple installer package

Run `brew cask install suspicious-package` or [download manually](http://www.mothersruin.com/software/downloads/SuspiciousPackage.pkg)

![](http://7q5cfr.com1.z0.glb.clouddn.com/SuspiciousPackage.png)

## [](https://github.com/sindresorhus/quick-look-plugins#more)More

_These are not included in [Install all](https://github.com/sindresorhus/quick-look-plugins#install-all)._

### [](https://github.com/sindresorhus/quick-look-plugins#provisionql)[ProvisionQL](https://github.com/ealeksandrov/ProvisionQL)

> Preview iOS / OS X app and provision information

Run `brew cask install provisionql` or [download manually](https://github.com/ealeksandrov/ProvisionQL/releases)

![](http://7q5cfr.com1.z0.glb.clouddn.com/ProvisionQL.png)

### [](https://github.com/sindresorhus/quick-look-plugins#other)Other

  * [CertQuickLook](https://code.google.com/p/cert-quicklook/) - preview various unprotected certificate tokens like X509 certificates, DER or PEM

## [](https://github.com/sindresorhus/quick-look-plugins#tip)Tip

Run this in your terminal to allow text selection in the Quick Look window:
    
    defaults write com.apple.finder QLEnableTextSelection -bool true && killall Finder


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