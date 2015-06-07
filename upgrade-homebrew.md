# upgrade-homebrew

在经历了升级正式版OS X的悲惨故事之后，说说这点事。如果你已经升级了，那么这可能是一个不愉快地过程。 

## 修复Homebrew 

1.编辑`/usr/local/Library/brew.rb`

2.修改ruby版本 

将 
    
    #!/System/Library/Frameworks/Ruby.framework/Versions/1.8/usr/bin/ruby -W0
    

改为 
    
    #!/System/Library/Frameworks/Ruby.framework/Versions/Current/usr/bin/ruby -W0
    

Save and exit brew.rb 

3.保存文件 

## 开发者升级Mac OS X 10.10 

1.做一个完整的备份 

2.移动`/usr/local`到一个安全的地方，系统会修改这个文件夹。。。 

3.升级 

4.将`/usr/local/`移动回来 