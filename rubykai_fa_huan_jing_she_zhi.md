# Ruby开发环境设置

## 安装RVM

Rvm是Ruby管理器。当系统需要同时安装多个Ruby的时候，RVM非常管用。官方默认的直接将rails一块安装了，我们并不需要，修改为：
    
    curl -L https://raw.github.com/wayneeseguin/rvm/master/binscripts/rvm-installer | bash -s stable --autolibs=enabled
    

注意其中的`--autolibs=enabled`参数，将自动将缺少的库，比如sqlite、openssl安装上。然后按照shell中的提示，重启RVM：
    
    rvm reload
    

## 安装Ruby

通过RVM安装Ruby：
    
       rvm install ruby
    

## 通过gem安装Rails

Ruby的插件管理器，叫做gem。通过gem安装Rails：
    
    gem instal rails
    

创建一个Rails项目，
    
    rails new blog 
    

本地测试：
    
    cd blog
    Rails s
    

## 设置shell默认的gem集合

Rails项目下面，会有一个文件，用于管理插件，叫做Gemfile。Gemfile配套的管理工具叫做bunlde：
    
    bundle check   #检查gem是否缺少
    bundle install #安装缺少的gem
    bundle update  #重新安装gem，更新项目文件下面的gemfile.lock文件
    

创建gemset，并使用gemset作为默认的开发环境：
    
    rvm use 2.1.0
    rvm gemset create blog #创建ruby2.0下面名为blog的gemset
    rvm use 2.1.0@blog --deault #将该gemset作为默认的Ruby开发环境
