# Installing Python on Linux（在Linux上安装Python）

> The latest versions of Ubuntu and Fedora come with Python 2.7 out of the box.

最新版的Ubuntu和Fedora自带Python 2.7，直接使用。

> The latest versions of Redhat Enterprise (RHEL) and CentOS come with Python 2.6. Some older versions of RHEL and CentOS come with Python 2.4 which is unacceptable for modern Python development. Fortunately, there are [Extra Packages for Enterprise Linux](http://fedoraproject.org/wiki/EPEL) which include high quality additional packages based on their Fedora counterparts. This repository contains a Python 2.6 package specifically designed to install side-by-side with the system’s Python 2.4 installation.

最新版的RHEL红帽子企业版和CentOS自带Python 2.6。一些老版本的系统自带Python 2.4，已经不能满足现代的Python开发者了。幸运的是，[Extra Packages for Enterprise Linux](http://fedoraproject.org/wiki/EPEL)包含基于Fedora系列的高质量附加包。这个仓库中包括一个Python 2.6的包，这是为与系统同时安装的Python 2.4特别设计的。

> You do not need to install or configure anything else to use Python. Having said that, I would strongly recommend that you install the tools and libraries described in the next section before you start building Python applications for real-world use. In particular, you should always install`Setuptools`, as it makes it much easier for you to use other third-party Python libraries.

你不需要安装和配置任何东西就可以使用Python，话虽如此，在你开始构建实际使用的Python程序之前，我强烈建议你安装在下一节中描述的工具和库。特别的是，你最应该安装`Setuptools`，因为它可以让你非常轻易得使用其他第三方Python库。

## Setuptools & Pip

> The most crucial third-party Python software of all is Setuptools, which extends the packaging and installation facilities provided by the distutils in the standard library. Once you add Setuptools to your Python system you can download and install any compliant Python software product with a single command. It also enables you to add this network installation capability to your own Python software with very little work.

最重要的第三方Python软件就是Setuptools，它能够扩展由标准库中的distutils提供的包装和安装设施。一旦你添加`Setuptools`到你的Python系统中，仅需一条命令就可以下载和安装任何兼容的Python软件产品。它也让你可以通过很少的工作量就将这种网络安装能力添加到自己的Python软件中。

> To obtain the latest version of Setuptools for Linux, refer to the documentation available here:[unix-setuptools](https://pypi.python.org/pypi/setuptools#unix-wget)

为了获得最新的Linux版本Setuptools，参考文档：[unix-setuptools](https://pypi.python.org/pypi/setuptools#unix-wget)

> The new [`easy_install`](https://pypi.python.org/pypi/setuptools#unix-wget) command you have available is considered by many to be deprecated, so we will install its replacement: `pip`. Pip allows for uninstallation of packages, and is actively maintained, unlike easy_install.

你现在拥有的新命令：`easy_install`已经被很多人弃用了，所以我们将安装它的替代品：`pip`。`pip`比`easy_install`好在它可以卸载一个包，还被积极维护着。

> To install pip, simply open a command prompt and run:

为了安装`pip`，只需简单打开命令行运行：
    
    $ easy_install pip
    

## Virtual Environments（虚拟环境）

> A Virtual Environment is a tool to keep the dependencies required by different projects in separate places, by creating virtual Python environments for them. It solves the “Project X depends on version [1](http://jimmylv.gitbooks.io/python-guide-zh/content/GLOSSARY.html#1).x but, Project Y needs 4.x” dilemma, and keeps your global site-packages directory clean and manageable.

Virtual Environment是一种隔离依赖的工具，通过创建虚拟Python环境来保持不同项目在单独的地方。它解决了“项目X依赖版本[1](http://jimmylv.gitbooks.io/python-guide-zh/content/GLOSSARY.html#1).x但是项目Y需要4.x”这种困境，可以保证你的总包目录是干净的和可管理的。

> For example, you can work on a project which requires Django [1](http://jimmylv.gitbooks.io/python-guide-zh/content/GLOSSARY.html#1).3 while also maintaining a project which requires Django [1](http://jimmylv.gitbooks.io/python-guide-zh/content/GLOSSARY.html#1).0.

例如，你可以在一个依赖Django [1](http://jimmylv.gitbooks.io/python-guide-zh/content/GLOSSARY.html#1).3的项目上工具，也可以同时维护一个需要Django [1](http://jimmylv.gitbooks.io/python-guide-zh/content/GLOSSARY.html#1).0的项目。

> To start using and see more information: [Virtual Environments](http://github.com/kennethreitz/python-guide/blob/master/docs/dev/virtualenvs.rst) docs.

开始使用，查看更多信息：[Virtual Environments](http://github.com/kennethreitz/python-guide/blob/master/docs/dev/virtualenvs.rst)文档。

> You can also use [virtualenvwrapper](http://docs.python-guide.org/en/latest/dev/virtualenvs/#virtualenvwrapper-ref) to make it easier to manage your virtual environments.

你也可以使用[virtualenvwrapper](http://docs.python-guide.org/en/latest/dev/virtualenvs/#virtualenvwrapper-ref)，让它更容易管理你的虚拟环境。
