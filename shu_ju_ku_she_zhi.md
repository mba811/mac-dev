# 数据库设置

## 安装postgresql数据库

#### 手动安装方法

这是手动通过brew进行安装的方法，如果是完全新手，跳到下一节，看更简单的安装方法。
    
    brew install postgresql
    postgres -D /usr/local/var/postgres
    

查看是否安装成功，版本是：
    
    psql --version
    

初始化数据库：
    
    initdb /usr/local/var/postgres -E utf8
    

查看brew下的postgresql，
    
    brew list postgresql
    

发现，postgresql版本是9.2.4。

请注意，`/usr/local/Cellar/postgresql/9.2.4/`的路径会跟随postgresql的版本变化而变化。未来记得修改为相应路径。

因此，输入下列命令，设为随机启动：
    
    mkdir -p ~/Library/LaunchAgents
    cp /usr/local/Cellar/postgresql/9.2.4/homebrew.mxcl.postgresql.plist ~/Library/LaunchAgents
    launchctl load -w ~/Library/LaunchAgents/homebrew.mxcl.postgresql.plist
    

更详细的参考文档：

  * [Migrating to PostgreSQL](http://railscasts.com/episodes/342-migrating-to-postgresql?view=asciicast)

#### 自动安装方法

一个简单的、自动安装Postgresql数据库的方法是，下载Postgresql App即可，网址是：

[Postgres.app | the easiest way to run PostgreSQL on the Mac](http://postgresapp.com/)

### 安装mysql数据库

安装mysql：
    
    brew install mysql
    

然后，启动mysql
    
    mysql.server start
    

请注意，按照brew的安装提示，将mysql设置为自动启动。
    
    ln -sfv /usr/local/opt/mysql/*.plist ~/Library/LaunchAgents
    

进入mysql数据库：
    
    mysql -uroot
    

### 数据库管理软件

[navicat premium](http://www.navicat.com/en/products/navicat_premium/premium_overview.html):商业收费软件。老牌的数据库管理客户端。 支持mysql、postgresql、sqlite与oracle等。

![Navicat Premium](http://www.yangzhiping.com/images/mac-2013-dev/navicat-premium.png)
