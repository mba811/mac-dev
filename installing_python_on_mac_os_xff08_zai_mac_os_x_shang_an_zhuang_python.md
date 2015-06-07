# Installing Python on Mac OS X（在Mac OS X上安装Python）

> The latest version of Mac OS X, Mavericks, **comes with Python 2.7 out of the box.**

最新版的Mac OS X系统Mavericks自带Python 2.7，可以立即使用。

> You do not need to install or configure anything else to use Python. Having said that, I would strongly recommend that you install the tools and libraries described in the next section before you start building Python applications for real-world use. In particular, you should always install`Setuptools`, as it makes it much easier for you to use other third-party Python libraries.

你不需要任何安装和配置就可以使用Python。话虽如此，在你开始构建实际使用的Python程序之前，我强烈建议你安装在下一节中描述的工具和库。特别的是，你最应该安装`Setuptools`，因为它可以让你非常轻易得使用其他第三方Python库。

> The version of Python that ships with OS X is great for learning but it’s not good for development. The version shipped with OS X may be out of date from the official current Python release, which is considered the stable production version.

附带自OS X的这个版本的Python是非常利于学习的，但是对开发来说并不友好。附带的版本可能与被认为是最稳定生产版本的官方最新发行版相比已经过时了。

## Doing it Right（正确安装Python）

> Let’s install a real version of Python.

让我们安装一个真正的Python版本。

> Before installing Python, you’ll need to install GCC. GCC can be obtained by downloading XCode, the smaller Command Line Tools (must have an Apple account) or the even smaller OSX-GCC-Installer package.

在安装之前，你需要安装GCC。GCC可以通过下载XCode获取，这是一个很小的命令行工具（必须要有Apple帐号），或者下载更小的OSX-GCC-Installer包。

> **Note:**
> 
> _If you already have XCode installed, do not install OSX-GCC-Installer. In combination, the software can cause issues that are difficult to diagnose._
> 
> **注意：**
> 
> 如果你已经安装了XCode，不在再安装OSX-GCC-Installer。如果重复了可能会导致难以诊断的问题。
> 
> While OS X comes with a large number of UNIX utilities, those familiar with Linux systems will notice one key component missing: a decent package manager. `Homebrew` fills this void.

虽然OS X附带了大量的UNIX实用工具，但是熟悉Linux系统的人可能会注意到缺少了一个关键组件：一个像样的包管理工具。Homebrew可以填补空白。

> To install `Homebrew`, open `Terminal` or your favorite OSX terminal emulator and run

为了安装`Homebrew`，打开`Terminal`或者你最喜欢的OSX终端模拟器，运行。
    
    $ ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
    

> The script will explain what changes it will make and prompt you before the installation begins. Once you’ve installed Homebrew, insert the Homebrew directory at the top of your `PATH`environment variable. You can do this by adding the following line at the bottom of your`~/.profile` file

这个脚本将会解释，在安装开始之前改变它会编译和提示你。一旦你已经安装Homebrew，将Homebrew目录插入到你的`PATH`环境变量的最前面。你可以在你的`~/.profile`文件底部添加以下代码：
    
    export PATH=/usr/local/bin:/usr/local/sbin:$PATH
    

> Now, we can install Python 2.7:

现在我们可以安装Python 2.7：
    
    $ brew install python
    

> This will take a minute or two.

这会花费一到两分钟

## Setuptools & Pip（包管理工具）

> Homebrew installs `Setuptools` and `pip` for you.

Homebrew可以为你安装`Setuptools`和`pip`。

> `Setuptools` enables you to download and install any compliant Python software over a network (usually the Internet) with a single command (`easy_install`). It also enables you to add this network installation capability to your own Python software with very little work.

`Setuptools`可以使你通过网络（通常是Internet）下载和安装任何兼容的Python软件，仅需一条简单的`easy_install`命令。它也让你通过很少的工作量就可以将这种网络安装能力添加到自己的Python软件中。

> `pip` is a tool for easily installing and managing Python packages, that is recommended over`easy_install`. It is superior to `easy_install` in several ways, and is actively maintained.

`pip`一种轻松安装和管理Python包的工具，比`easy_install`更受欢迎。它在几个方面优于`easy_install`，并积极维护。

## Virtual Environments（虚拟环境）

> A Virtual Environment is a tool to keep the dependencies required by different projects in separate places, by creating virtual Python environments for them. It solves the “Project X depends on version [1](http://jimmylv.gitbooks.io/python-guide-zh/content/GLOSSARY.html#1).x but, Project Y needs 4.x” dilemma, and keeps your global site-packages directory clean and manageable.

Virtual Environment是一种隔离依赖的工具，通过创建虚拟Python环境来保持不同项目在单独的地方。它解决了“项目X依赖版本[1](http://jimmylv.gitbooks.io/python-guide-zh/content/GLOSSARY.html#1).x但是项目Y需要4.x”这种困境，可以保证你的总包目录是干净的和可管理的。

> For example, you can work on a project which requires Django [1](http://jimmylv.gitbooks.io/python-guide-zh/content/GLOSSARY.html#1).3 while also maintaining a project which requires Django [1](http://jimmylv.gitbooks.io/python-guide-zh/content/GLOSSARY.html#1).0.

例如，你可以在一个依赖Django [1](http://jimmylv.gitbooks.io/python-guide-zh/content/GLOSSARY.html#1).3的项目上工具，也可以同时维护一个需要Django [1](http://jimmylv.gitbooks.io/python-guide-zh/content/GLOSSARY.html#1).0的项目。

> To start using and see more information: [Virtual Environments](http://github.com/kennethreitz/python-guide/blob/master/docs/dev/virtualenvs.rst) docs.

开始使用，查看更多信息：[Virtual Environments](http://github.com/kennethreitz/python-guide/blob/master/docs/dev/virtualenvs.rst)文档。
