# 在Brew中添加新的软件

在homebrew中，有些软件并不是默认就存在的。比如这个 [Betty](http://jandan.net/2014/05/08/betty.html)。查了一下，在homebrew的Formula列表中的确是存在的。

那好吧，接下来，通过这几个步骤，轻松搞定。

1. 创建新的Formula

    brew create betty

2. 打开github上formula的内容。  
用浏览器，猛击 [betty.rb](https://github.com/timgaleckas/homebrew/blob/a098108d8ccc998406fe0e0a26749d5f7b0ea2b0/Library/Formula/betty.rb)

    brew edit betty

并将网页上rb里的代码都粘到brew edit中。

3. 安装betty

    brew install betty

