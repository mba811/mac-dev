# github工作流程设置

### 使用.dotnetfiles统一管理git配置

使用之前`git clone`下来的`.dotnetfiles`来管理git等很多配置文件。创建软链接：
    
    ln -s ~/.dotfiles/git/gitconfig ~/.gitconfig
    ln -s ~/.dotfiles/git/gitignore_global ~/.gitignore_global
    

请特别注意，将其中的~/.dotfiles/git/gitconfig目录中得内容修改为自己的Email地址、Github用户名等。

### 配置github的SSH秘钥

按照[Github提示](https://help.github.com/articles/generating-ssh-keys)，创建SSH秘钥：
    
    mkdir ~/.ssh #创建ssh命令
    cd ~/.ssh
    ssh-keygen -t rsa -C "your_email@example.com" #注意更改Email地址
    pbcopy < ~/.ssh/id_rsa.pub
    

此时，pdcopy命令已经将id_rsa.pub内容复制到剪切板。登陆github：

[https://github.com/settings/ssh](https://github.com/settings/ssh)

点击`Add an SSH Key`，`Title` 部分填写一个所用电脑的名称，然后在`Key`部分填写之前通过pdcopy命令复制的内容。

![Githu Ssh](http://www.yangzhiping.com/images/mac-2013-dev/githu-ssh.png)

### github最常用的命令

备份到github上：
    
    git add .
    git commit -a -m"今天的修改内容是。。。"
    git push ##只有这一步骤才需要联网
    

设置自己的github所在的分支：
    
    git branch --list
    git branch psytown
    git checkout psytown
    #第一次推送的时候得查文档
    

### 安装git flow

安装git-flow
    
    brew install git-flow
    

使用git flow 初始化项目。
    
    git flow init
    

创建所有的分支。按照git-flow默认提示即可。

比如，将数据库切换为postgresql。命名一个名为postgresql的新分支。
    
    git flow feature start postgresql
    

编辑之后，按照正常git流程处理。比如：
    
    git add .
    git commit -am "一些改动"
    

使用此命令完成此新特征的测试：
    
    git flow feature finish postgresql
    

如下图所示：

![Git Flow 2013](http://www.yangzhiping.com/images/mac-2013-dev/git-flow-2013.png)

更详细的参考文档：

  * [Git flow 開發流程](http://ihower.tw/blog/archives/5140)
  * [Git-flow 使用笔记](http://fann.im/blog/2012/03/12/git-flow-notes/)