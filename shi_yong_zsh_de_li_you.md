# 使用 Zsh 的理由

像大部分 *nix 用户，我之前用 bash 很多年，期间也有过小的不爽，但一直都忍过来，或者是说没想过这些不爽的地方能解决，比如 `cd` 到一个深目录时得哐哐猛敲 `<TAB>`。这么多年里我也尝试过其他 shell。比如 ksh/tcsh 以及今天要说的 zsh，但最终都没坚持下去，因为心中始终还是认为 bash 是最正统的 shell，不愿意去主动深入学习其他 shell。直到前几天逛 github，发现 [排名第 6 的开源项目 oh-my-zsh](https://github.com/popular/forked)，下来试用了一把，顿时觉得 bash 各种操作不爽到无法忍受。

**放弃 bash 的各种内牛满面的理由**

这里有个 youtube 上的视频，短短 4 分钟就已经抛出了几十个让 bash 用户切换到 zsh 中的理由。[视频链接](http://youtu.be/HGBgMX5HW_g)

**理由 0：zsh 兼容 bash**

兼容 bash 意味着我不需要太多学习成本就可以切换过来，意味着我以前在 bash 下积累的 shell 语法、基本操作都不会荒废。在我心里 bash 还是最通用和标准的 shell 环境，因此兼容 bash 让我切换到 zsh 时没有太多后顾之忧。

**理由 1：zsh 的补全模式更方便**

zsh 中按两下 tab 键可以触发 zsh 的补全，所有待补全项都可以通过键盘方向键或者 `<Ctrl-n/p/f/b>` 来选择。

[[![nine reasons to use zsh](http://jbcdn2.b0.upaiyun.com/2012/09/nine-reasons-to-use-zsh.png)](http://jbcdn2.b0.upaiyun.com/2012/09/nine-reasons-to-use-zsh.png)nine reasons to use zsh](http://jbcdn2.b0.upaiyun.com/2012/09/nine-reasons-to-use-zsh.png)

**理由 2：zsh 支持命令选项补全**

zsh 除了支持目录的补全，还支持命令选项的补全，例如 `ls -<TAB><TAB>` 会直接列出所有 `ls` 的参数，再也不会出现一个命令打到一半，忘记参数导致重开一个 terminal `man` 一把。

[[![nine reasons to use zsh](http://jbcdn2.b0.upaiyun.com/2012/09/nine-reasons-to-use-zsh-2.png)](http://jbcdn2.b0.upaiyun.com/2012/09/nine-reasons-to-use-zsh-2.png)nine reasons to use zsh](http://jbcdn2.b0.upaiyun.com/2012/09/nine-reasons-to-use-zsh-2.png)

**理由 3：zsh 支持命令参数补全**

以前想 `kill` 掉一个进程，我的做法是 `ps aux | grep "进程名"` 然后记下 id，再 `kill id`。在 `zsh` 下，只需要 `kill 进程名<TAB>`，`zsh` 就会自动补全进程的 pid。

[[![nine reasons to use zsh](http://jbcdn2.b0.upaiyun.com/2012/09/nine-reasons-to-use-zsh-3.png)](http://jbcdn2.b0.upaiyun.com/2012/09/nine-reasons-to-use-zsh-3.png)nine reasons to use zsh](http://jbcdn2.b0.upaiyun.com/2012/09/nine-reasons-to-use-zsh-3.png)

其余我常用的补全还有：

`·ssh <TAB><TAB>` 时 zsh 会自动列出你访问过的主机和用户名来补全 `ssh` 的参数。  
`·brew install <TAB><TAB>` 来补全软件包名，除了 homebrew 以外，同样支持 port/apt-get 等其他包管理器。

**理由 4：zsh 支持更加聪明的目录补全**

以前比如想进入一个比较深的目录，比如 `/Users/pw/workspace/project/src/main/webapps/static/js`，就得在 bash 下面打半天，不停的 tab 去补全一个正确的路径出来。在 zsh 下，只需要输入每个路径的头字母然后 tab 一下： `cd /u/p/w/p/s/m/w/s/j<TAB>`

**理由 5：zsh 强大的快速目录切换**

以前最苦逼的事情莫过于频繁在两个工作目录下切换，总要打一长串 `cd` 路径。也尝试过 `popd` 和 `pushd` 来解决这个问题，但往往是目录已经切换了才想起来没用 `pushd`。而 zsh 会记住你每一次切换的路径，然后通过 `1` 来切换到你上一次访问的路径，`2` 切换到上上次……一直到 `9`，还可以通过 `d` 查看目录访问历史。

zsh 还可以配合 autojump 一起使用，autojump 会记录下每一个你访问过的目录，然后通过 `j` 来快速跳转。

**理由 6：zsh 支持全局 alias 和后缀名 alias**

bash 的 `alias` 只能做命令的缩写，而 `zsh` 更进一步，使 `alias` 可以缩写命令的一部分，例如参数或环境变量设置。

    
    alias -s log=less
    
    ~/package/tomcat/log/catalina.log # 相当于 less ~/package/tomcat/log/catalina.log
    
    alias -g PR=http_proxy=127.0.0.1:8087
    
    PR curl https://twitter.com # 相当于 http_proxy=127.0.0.1:8087 curl https://twitter.com

**理由 7：zsh 有着丰富多彩的命令行提示符**

bash 下通过设置 `$PS1` 已经可以实现很丰富的提示符了，而 zsh 更进一步，可以实现诸如多行提示符、提示符右对齐等功能。`oh-my-zsh` 配置文件中提供了非常丰富的提示符 theme 供选择，我使用的是 `gentoo` 主题，比较简洁，还可以显示当前 git 仓库的状态。

**理由 8：zsh 有更多优雅的语法**

例如修改 `PATH`，bash 下设置 `$PATH` 要求所有路径都要写在一行里，目录多了以后看起来就很难看。zsh 支持更加符合程序员审美观的设置方式。
    
    
    path=(
    
        ~/bin
    
        $path
    
        ~/package/smartsprites/bin
    
    )

**安装 zsh**

Linux 用户通过各自发行版的包管理器直接安装即可。

Mac 自带一个 4.x.x 版本的 zsh，可以直接使用，也可以通过 homebrew 安装最近刚刚发布的 5.0.0 版本。推荐使用最新的 5.0 版本，对多字节字符提供了完整的支持，这一点对于国内用户来说很重要。[详细的 release note](http://zsh.sourceforge.net/releases.html)

**设置为默认 shell**

通过命令 `chsh` 修改默认登录 shell，需要注意的是，如果通过 homebrew 安装了最新版本的 zsh，则需要 `sudo` 编辑`/etc/shells` 加入一行 `/usr/local/bin/zsh`。然后再通过 `chsh` 来修改默认 shell，否则会提示 `/usr/local/bin/zsh` 不是合法的 shell。

**安装 oh-my-zsh 配置**

对于每一个像我这样的 zsh 初级用户来说，oh-my-zsh 就是救人于水火中的大杀器，强烈建议使用此配置上手 zsh。

作者提供了傻瓜安装命令：
    
    <code>curl -L https://github.com/robbyrussell/oh-my-zsh/raw/master/tools/install.sh | sh </code>
    

也可以手工安装，[具体步骤](https://github.com/robbyrussell/oh-my-zsh#the-manual-way)。

**几个必备的插件**

**autojump**

帮助快速目录跳转的小工具。首先要安装 autojump，然后在 `.zshrc` 中开启 autojump 插件。它会记录下来每个你进入过的目录，随后通过 `j 目录名称的一部分`就可快速跳转到该目录。 [Youtube 视频介绍](http://youtu.be/tnNyoMGnbKg)

**git**

Git 命令补全，除了可以补全 git 的子命令、命令开关等常规补全项以外，还可以补全分支名等内容，用 git 必开的插件。

**osx**

提供一些与 Mac OSX 系统交互的命令，比如：

**● **man-preview 通过 preview 程序查看一个命令的手册，例如 `man-preview git`

**● **quick-look 快速预览文件

**● **pfd 返回当前 finder 打开的文件夹的路径

**● **cdf 切换到当前 finder 所在的目录

### 相关文章

  * [Bash脚本：怎样一行行地读文件（最好和最坏的方法）](http://blog.jobbole.com/72185/)
  * [写出健壮的Bash脚本](http://blog.jobbole.com/15668/)
  * [Bash One-Liners Explained （二）：操作字符串](http://blog.jobbole.com/49843/)
  * [37条常用Linux Shell命令组合](http://blog.jobbole.com/48173/)
  * [学习Emacs：Zsh 和 Multi-Term](http://blog.jobbole.com/51598/)
  * [让你的Git水平更上一层楼的10个小贴士](http://blog.jobbole.com/75348/)
  * [理解Linux Shell和基本Shell脚本语言的小贴士（一）](http://blog.jobbole.com/63952/)
  * [一个备份MySQL数据库的简单Shell脚本](http://blog.jobbole.com/18005/)
  * [Bash One-Liners Explained（一）：文件处理](http://blog.jobbole.com/49800/)
  * [简洁的bash编程技巧](http://blog.jobbole.com/29973/)
