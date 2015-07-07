# Gate One

> HTML5终端模拟器/SSH客户端[Gate One](http://liftoffsoftware.com/Products/GateOne)发布了[v1.1版](https://github.com/liftoff/GateOne/downloads)。主要新特性包括：安全增强，性能改进，移动浏览器支持，改进终端模拟，系统日志信息的自动语法高亮，捕捉以及以图像形式展示PDF，Python 3支持，IE10支持，等等。官方DEMO演示显示你可以在浏览器上尝试vim，玩终端游戏，在lynx中冲浪，等等。

官方给出了RPM，DEB安装包唯独没有mac下的安装包，由于该项目太新，也就不指望homebrew安装了，只能选择从源码安装。

### 准备

根据[官方的安装指南](http://liftoff.github.com/GateOne/About/index.html#installation),安装前置需求软件：

软件版本

Python
2.6+ 或者 3.2+

Tornado Framework
2.2+

终端执行如下命令验证
    
    user@modern-host:~ $ python -V 
    Python 2.7.2+ 
    user@modern-host:~ $ python -c "import tornado;print(tornado.version)" 
    2.4 
    

若tornado没有安装，执行如下命令安装
    
    user@modern-host:~ $ sudo pip install tornado kerberos
    

### 安装

执行如下命令即可完成安装，安装目录位于/opt/gateone
    
    user@whatever:~ $ tar zxvf gateone*.tar.gz; cd GateOne*; sudo python setup.py install
    

由于gateone依赖dtach和PIL，如果没有安装这两个东西，启动的时候会提示某些功能会失效
    
    $ brew install dtach
    $ sudo pip install PIL
    

### 启动
    
    $ cd /opt/gateone
    $ sudo ./gateone.py
    

在chrome浏览器打开[https://127.0.0.1%E5%8D%B3%E5%8F%AF%E3%80%82](https://127.0.0.xn--1-qx8awo./)
