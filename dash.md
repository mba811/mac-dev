# DASH

可以下载并查看各种语言和引擎的文档，如Cocos2d、jQuery、html、javascript等，离线看文档非常方便。
下载地址：https://itunes.apple.com/cn/app/dash-docs-snippets/id458034879?mt=12

![](http://img.blog.csdn.net/20130822150905593?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvemhhb3h5Mjg1MA==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)


##Dash：程序员的的好帮手

作为一名死coder，每天最常见的动作就是查看各种API文档，你一定也有过同时打开N个窗口（HTML、PDF、CHM），不停的在编辑器与文档之间切换的感受吧？怎么说呢，其实我很讨厌这种枯燥无味的动作![](http://scriptfans.iteye.com/images/smiles/icon_cry.gif)，那么如何才能提高效率，减少无用功呢？下面就给大家介绍一款非常好用的Mac小工具：Dash，相比这个英文名，我跟喜欢叫它“叮当猫”，嘿嘿。

![Dash Icon](http://a1.mzstatic.com/us/r1000/106/Purple/v4/14/50/16/14501624-f6fd-4dae-a2bf-187a5a6417de/icon.175x175-75.png)

[点我直达AppStore介绍页面](http://itunes.apple.com/cn/app/dash-docs-snippets/id458034879?mt=12)

### 功能简介

官方用一句话就概括了它的用途：Dash是一个API文档浏览器（ API Documentation Browser），以及代码片段管理工具（Code Snippet Manager）。你没看错，它就只有这两个功能，但确实是程序员（至少对于我来说）最为关心的特性，自己之前也用过了不少类似的工具，可以毫不夸张地说，Dash是它们之中做的最好的一个！

### 强悍的API文档浏览、搜索功能

想必这个功能是大家最常用的了吧，每天要反复查看、搜索那么多的API细节，没有一个好工具，单靠自己的双手如何应付得来？窗口不停的切来切去，很烦啊！Dash采用集成单一窗口的方式，很好的解决了这个问题。看下面的截图：

  
![](http://dl.iteye.com/upload/attachment/0068/7591/80db8278-4de8-3916-bc7a-4ba63c832696.jpg)

上图便是Dash的API浏览器主界面：左侧边栏是各种编程语言以及框架（取决于你下载安装了多少文档集合）的导航大纲，点击某个节点，右边的内容区域就是文档的详细信息啦，非常直观。也可以在左上方的搜索框内通过输入关键字，查找相关的API文档，非常类似全文检索的实现方式，Dash的响应速度非常快！关键是可以同时查询不同的语言、框架内容，实在是太方便了。看到这里你也许要问了，这跟我们平常切换到特定的文档窗口（比如一个PDF或者一个CHM文件），再ctrl + f查找有什么区别，不是多此一举吗？其实你错了，Dash可以通过快捷键来显示、隐藏文档窗口，它提供了配置界面以便用户自行设置（我比较习惯alt+space，因为其他软件很少用到这个组合键）：
  
![](http://dl.iteye.com/upload/attachment/0068/7595/9f31cd95-0188-3cf2-801c-09d7f3206503.jpg)

Dash自带了丰富的API文档，涉及各种主流的编程语言和框架，全列出来很吓人的：

ActionScript, Android, C++, Cappuccino, Cocos2D, Cocos3D, Corona, CSS, Django, Groovy, HTML, Java, JavaFX, JavaScript, jQuery, Kobold2D, Lua, MySQL, Node.js, Man Pages, Perl, PHP, Python, Ruby, Ruby on Rails, Scala, Sparrow, SQLite, Unity 3D, WordPress, XSLT, XUL

而且它的文档库采用了docset格式，高级用户基于网站提供的教程，很容易就能自行添加其他的扩充文档，其实Dash在最初发布的时候，只支持很少的几个文档浏览，好像只有Java、HTML、CSS这些，是后来通过用户不断贡献，以及作者及时的反馈（Rails API就是我通过Email与作者联系，请求添加的，作者非常nice），逐步壮大，才具备了如此广泛的语言、框架支持。要添加API文档，打开软件配置界面，切换到Docset选项卡即可看到所有内置的文档列表，按需要自行下载即可（如果是自己制作的docset，双击即可导入Dash）：

![](http://dl.iteye.com/upload/attachment/0068/7608/6a6eb4b0-294a-31ae-b121-5c005e2b5a87.jpg)

### 牛逼、好用的代码片段管理功能

前面说完了Dash的文档查询功能，下面再来看一看它带给我们的另一个惊喜：代码片段管理。说到这里，之前的版本其实有个很不好的地方，就是如果不仔细琢磨一下，或者去看官方的帮助文档的话，用户是很难一眼就知道怎么用这个功能，新手引导做得确实不怎么样，不过最新版已经改善了这个问题，在主界面的导航边栏明确地给出了分类提示，创建或者修改代码片段都方便了许多。来看下面这个例子：

![](http://dl.iteye.com/upload/attachment/0068/7604/3c74be98-c3cc-37be-b30f-d6f1b91b43a2.jpg)

利用Dash的代码片段管理功能，我们可以把日常使用频繁（也就是你经常需要复制粘贴）的代码保存起来，然后为其设置一个独一无二的缩写，这样一来原本需要一遍又一遍的敲击键盘重复录入的繁琐工作，就可以交给Dash来帮你搞定啦。比如上面截图中的例子，就是ExtJS中发起Ajax请求的代码片段，哪怕是copy & paste，时间长了也会很烦的，我给它设置了一个缩写（ajax），以后在需要编写这段代码的时候，就只需要敲击这几个字母，它就会魔法般的出现在光标所在位置啦！很神奇吧？嘿嘿，其实这种扩展缩写的功能，还有很多软件都能做到，比如TextExpander（这个我也买了，半价14刀的时候，但是现在已经打入冷宫了，比较后悔），不过就用户体验和各种细节，诸如界面UI，特别是扩展占位符的处理上，目前还没有哪一个能比得过Dash的（Dash is the best!）。来看看使用代码片段的截图吧：
  
![](http://dl.iteye.com/upload/attachment/0068/7625/171644f8-cc2b-3b90-8920-2e506a4d9265.jpg)

Dash的缩写扩展功能很强大，比方说上面那个例子，在保存代码片段的时候，你可以使用双下划线标明占位符，在执行扩展的时候就可以通过tab键来在各个占位符之间切换，根据需要输入实际的值，最后回车即可把片段粘贴到光标所在之处。除了占位符，它还支持下面这些变量符号：

  * @clipboard 自动插入当前剪贴板中的内容
  * @cursor 代码片段粘贴完毕之后，自动将光标定位到此处
  * @date 自动插入当前日期
  * @time 自动插入当前时间

介绍到这里，各位看官，你应该已经深深滴爱上Dash了吧？每个苦逼的程序员，都应该有这么一只可爱贴心的叮当猫，您说是不是？其实个人不是很喜欢它的图标，实在是有点太诡异了，嘿嘿……

最后再说一句，Dash在Mac App Store里面免费提供下载，不过作者包含了一个IAP（应用程序内购买）插件，作者挺幽默的，看介绍是说的Dash的双胞胎伙伴Pinky比较调皮，会时不时的跳出来打扰你一下，囧……反正我运行了一晚上，还没见到这只传说中的猫呢。其实这只不过是给你提供了赞助作者的机会，毕竟这么好的软件，如果经济条件允许，支持一下也无可厚非，同是软件开发者，其中的辛酸你我都懂的。