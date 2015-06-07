# Homebrew versions安装特定版本软件

## brew versions 

出现了下面的错误 
    
    brew versions gradle
    Error: Unknown command: versions
    

原因是在更新Mac OS的时候一些东西已经没了 

## brew versions install 

所以需要tap这个 
    
    brew tap homebrew/boneyard
    

接着就可以使用`brew versions`
    
    Warning: brew-versions is unsupported and will be removed soon.
    You should use the homebrew-versions tap instead:
      https://github.com/Homebrew/homebrew-versions
    
    2.1      git checkout 5475eb4 /usr/local/Library/Formula/gradle.rb
    2.0      git checkout 94fcdae /usr/local/Library/Formula/gradle.rb
    1.12     git checkout 8ef0672 /usr/local/Library/Formula/gradle.rb
    1.11     git checkout 01f2e6f /usr/local/Library/Formula/gradle.rb
    1.10     git checkout c6baa40 /usr/local/Library/Formula/gradle.rb
    1.9      git checkout 5bab5e9 /usr/local/Library/Formula/gradle.rb
    1.8      git checkout 9214e60 /usr/local/Library/Formula/gradle.rb
    1.7      git checkout f826cc9 /usr/local/Library/Formula/gradle.rb
    1.6      git checkout fff7c0b /usr/local/Library/Formula/gradle.rb
    1.5      git checkout 57931e0 /usr/local/Library/Formula/gradle.rb
    
