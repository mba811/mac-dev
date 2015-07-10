# Homebrew

包管理工具可以让你安装和更新程序变得更方便，目前在 OS X 系统中最受欢迎的包管理工具是 [Homebrew](http://brew.sh/).

### 安装

在安装 Homebrew 之前，需要将 **Xcode Command Line Tools** 安装完成，这样你就可以使用基于 Xcode Command Line Tools 编译的 Homebrew。

在 terminal 中复制以下命令（不包括 `$`），跟随指引，将完成 Hombrew 安装。

    $ ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

紧接着，我们需要做一件事让通过 Homebrew 安装的程序的启动链接 (在 `/usr/local/bin`中）可以直接运行，无需将完整路径写出。通过以下命令将 `/usr/local/bin` 添加至 `$PATH` 环境变量中:

    $ echo 'export PATH="/usr/local/bin:$PATH"' >> ~/.bash_profile

**Cmd+T** 打开一个新的 terminal 标签页，运行以下命令，确保 brew 运行正常。

    $ brew doctor

---
`译注：`

安装完成后，Homebrew 会将本地 `/usr/local` 初始化为 git     的工作树，并将目录所有者变更为当前所操作的用户，将来 `brew` 的相关操作不需要 sudo 。
