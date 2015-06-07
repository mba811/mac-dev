# Yosemite 10.10 开发者升级

之前在苹果放出mac os 10.10 beta2的时候试着升级了一下，然后发现了一个又一个的坑，又没有用Time Machine备份，只能继续一步步下去。 

## 修改MACOSX_DEPLOYMENT_TARGET 

因为某些原因会导致编译的时候出问题，所以先把这个放在最上面。 
    
    export MACOSX_DEPLOYMENT_TARGET=10.9
    

## Mac OS JDK 1.6 

1.下载JDK1.6 

由于项目上的Java版本仍然是1.6，所以这时就需要重新安装一下这个版本的JAVA。 

苹果官方提供了一个旧版本的Java 

下载地址: [Java for OS X 2014-001][1]

   [1]: http://support.apple.com/kb/DL1572

2.配置 

指向旧版本的JDK 
    
    export JAVA_HOME="/System/Library/Frameworks/JavaVM.framework/Home/"
    

当然你也可以这样子 

### ondir 

ondir是一个小程序来自动针对特定目录的任务。它的工作原理是在目录中执行脚本，当你进入和离开目录的时候。 

1.安装ondir 
    
    brew install ondir
    

2.配置，在.bash_profile添加下面的内容 
    
    cd()
    {
        builtin cd "$@" && eval "`ondir \"$OLDPWD\" \"$PWD\"`"
    }
    
    pushd()
    {
        builtin pushd "$@" && eval "`ondir \"$OLDPWD\" \"$PWD\"`"
    }
    
    popd()
    {
        builtin popd "$@" && eval "`ondir \"$OLDPWD\" \"$PWD\"`"
    }
    
    eval "`ondir /`"
    

3.配置到.ondirrc 
    
    enter ~/java
       echo "export JAVA_HOME='/System/Library/Frameworks/JavaVM.framework/Home/'"
       export JAVA_HOME="/System/Library/Frameworks/JavaVM.framework/Home/"
    

## Mac OS 10.10 rvm rbenv 

由于某种原因我们用`rvm install ruby`的时候会出错 
    
    Error running '__rvm_with ruby-1.9.3-p547 env CFLAGS=-I/usr/local/opt/libyaml/include -I/usr/local/opt/readline/include -I/usr/local/opt/libksba/include -I/usr/local/opt/openssl098/include LDFLAGS=-L/usr/local/opt/libyaml/lib -L/usr/local/opt/readline/lib -L/usr/local/opt/libksba/lib -L/usr/local/opt/openssl098/lib ./installer -a /Users/fdhuang/.rvm/rubies/ree-1.8.7-2012.02 --no-tcmalloc --dont-install-useful-gems -c --without-tcl -c --without-tk -c --disable-install-doc -c --enable-shared',
    showing last 15 lines of /Users/fdhuang/.rvm/log/1410957162_ree-1.8.7-2012.02/install.log
    cp ../.././ext/nkf/lib/kconv.rb ../../.ext/common
    compiling openssl
    /usr/local/opt/gcc46/bin/gcc-4.6 -I/opt/local/include -I. -I/opt/local/include -I../.. -I../../. -I../.././ext/openssl -DRUBY_EXTCONF_H=\"extconf.h\"  -D_XOPEN_SOURCE -D_DARWIN_C_SOURCE   -fno-common -g -O2 -I/usr/local/opt/libyaml/include -I/usr/local/opt/readline/include -I/usr/local/opt/libksba/include -I/usr/local/opt/openssl098/include  -fno-common -pipe -fno-common   -c openssl_missing.c
    In file included from openssl_missing.c:22:0:
    openssl_missing.h:71:6: error: conflicting types for 'HMAC_CTX_copy'
    /opt/local/include/openssl/hmac.h:102:5: note: previous declaration of 'HMAC_CTX_copy' was here
    openssl_missing.h:95:5: error: conflicting types for 'EVP_CIPHER_CTX_copy'
    /opt/local/include/openssl/evp.h:502:5: note: previous declaration of 'EVP_CIPHER_CTX_copy' was here
    openssl_missing.c:26:1: error: conflicting types for 'HMAC_CTX_copy'
    /opt/local/include/openssl/hmac.h:102:5: note: previous declaration of 'HMAC_CTX_copy' was here
    openssl_missing.c:120:1: error: conflicting types for 'EVP_CIPHER_CTX_copy'
    /opt/local/include/openssl/evp.h:502:5: note: previous declaration of 'EVP_CIPHER_CTX_copy' was here
    make[1]: *** [openssl_missing.o] Error 1
    make: *** [all] Error 1
    ++ return 1
    

而这里的错指向的是openssl，而之前还是好的，这时试了试传闻已久的rbenv。rvm已经不推荐使用了，至少还和上面的ondir不兼容。 

1.卸载rvm 
    
    rvm implode
    

2.安装rbenv 
    
    brew install rbenv
    

3.添加到环境变量中 
    
    export PATH="$HOME/.rbenv/bin:$PATH"
    eval "$(rbenv init -)"
    

## Mac OS 10.10 MacPorts 安装 

无法真正衡量port与brew地优与劣，有时候还是挺喜欢port的，比如需要某些组件的时候，而在当前port还不支持mac os，于是需要手动去编译。 

1.下载Mac Ports 
    
    wget https://distfiles.macports.org/MacPorts/MacPorts-2.3.1.tar.gz
    tar xzvf MacPorts-2.3.1.tar.gz
    

2.编译与安装 
    
    cd MacPorts-2.3.1
    ./configure && make && sudo make install