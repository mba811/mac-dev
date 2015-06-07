# 常用shell命令

### which命令

当你不知道现在用的是哪个路径所使用的ruby、python时，常使用which命令：
    
    which ruby
    which python
    which R
    

### 查询版本

确认是否安装成功时、安装的是什么版本的时候，使用该命令。如：
    
    ruby --version
    python --version
    curl --version
    

shell命令常有一个规律，一般--后面带单词的全拼，如version，-后面带单词的首字字母，如：-V。所以，不少时候可以精简为：
    
    ruby -v
    python -v
    

但是，此规律对curl等例外，此时，往往是需要大写，如：
    
    curl -V
    

### 帮助

查询帮助时，遵从同样的规律，如：--help或者-h。比如：
    
    ruby --help
    python --help
    

或者：
    
    ruby -h
    python -h
    

将列出ruby的主要命令。当然，也有只支持--help的，如：
    
    git --help 
    

### 路径相关

进入某个目录：
    
    cd ~/
    

查询当前目录：
    
    pwd
    

创建目录：
    
    mkdir  blog
    

删除目录：
    
    rm -rf blog
    

打印系统所使用的PATH命令：
    
    $PATH
    

编辑系统所在的path先后次序：
    
    subl /etc/paths