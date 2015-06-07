# Python开发环境配置

## 配置Python开发环境

首先通过brew，在iterm2中安装Python。
    
    brew install python
    

检查Python是否安装成功：
    
    Python -V
    

然后再创建一个专用目录，比如叫做：`~/.virtualenvs`，用于保存python的开发环境信息。
    
    mkdir ~/.virtualenvs
    cd ~/.virtualenvs
    

接下来，通过pip包（类似于Ruby中的gem、R中的cran，Python中的包管理机制），安装Python虚拟环境库virtualenv
    
    pip install virtualenv
    

然后，假设我们要开发项目，创建一个该项目专用开发环境，假设命名为：`myproject`
    
    virtualenv myproject
    

创建成功之后，我们会发现，在我们上一步创建的`~/python`目录下面就多了一个`django/bin/python`的目录，相关第三方包等内容以后都回下载在这里。我们只需要激活该环境即可：
    
    source ~/.virtualenvs/myproject/bin/activate
    

如果此时，zsh与oh-my-zsh已经配置成功，iterm2会提醒我们，Python开发环境已经切换到`myproject`下来。如下图所示：

![Django](http://www.yangzhiping.com/images/python/django.png)

接下来，在该环境下，安装相关django等类库即可。
    
    pip install django
    
    更详细的可参考：
    

  * [Introduction — virtualenv 1.11.2 documentation](http://www.virtualenv.org/en/latest/virtualenv.html#installation)

Python开发，既可以使用Texmate或者sublimetext，也可以使用PyCharm这一类Python IDE。