# OS X 命令行运行Sublime Text 2

Vim很快捷，但是在GUI下面似乎还是Sublime Text 给力，Sublime没有像RubyMine或者是PyCharm那么高大上，可以直接将用命令启动。所以。。 

1.添加link 
    
     ln -s /Applications/Sublime\ Text\ 2.app/Contents/SharedSupport/bin/subl /usr/local/bin/subl
    

2.编辑PATH 
    
    vim ~/.bash_profile
    

3.添加PATH 
    
     export PATH=/usr/local/bin:$PATH
    

4.应用 
    
     source ~/.bash_profile
    
