>Atom 使用手册

# 入门

## 为什么使用 Atom

有很多文本编辑器在那里，为什么你应该花时间了解并使用凌动？

编辑一样崇高和TextMate的报价方便，但只有有限的可扩展性。在光谱的另一端，Emacs和Vim提供了极大的灵活性，但他们不是很平易近人，只能用专用的脚本语言进行定制。

我们认为我们可以做的更好。我们的目标是可编程性和可用性的零妥协的组合：将欢迎到一所小学的学生在他们的第一天学习代码编辑器，但也是一个工具，他们不会长大，他们发展成为经验丰富的黑客。

由于我们使用的Atom打造的Atom，什么开始作为一个实验已逐渐成熟，成为我们生活中不可缺少的工具。从表面上看，Atom是你所期待的现代桌面文本编辑器。然而，流行的引擎盖，你会发现乞讨被砍死在一个系统中。

### [](https://atom.io/docs/latest/getting-started-why-atom#the-nucleus-of-atom)原子核

该网站是不是没有错，但二十年的发展已经锻造成一个令人难以置信的可塑性和功能强大的平台。所以，当我们开始着手编写我们自己想延长一个文本编辑器，网络技术是显而易见的选择。但首先，我们不得不从它的锁链下解放它。

#### [](https://atom.io/docs/latest/getting-started-why-atom#the-native-web)在本地网络

Web浏览器是伟大的浏览网页，但编写代码是值得的专用工具的专业活动。更重要的是，浏览器严格限制访问出于安全原因，本地系统，并为我们，不能写入文件或运行本地子过程文本编辑器是一个非首发。

出于这个原因，我们没有建立原子作为一个传统的Web应用程序。相反，原子是铬的一个专门变体设计为一个文本编辑器，而不是一个网络浏览器。每原子窗口实质上是一个本地渲染网页。

所有提供给一个典型的Node.js应用的API也可用于在每个窗口的JavaScript的上下文中运行的代码。这种混合提供了一个真正独特的客户端开发经验。

既然一切都是本地的，你不必担心资产管道，剧本串联，和异步模块定义。如果你想加载一些代码，只是要求它在你的文件的顶部。节点的模块系统可以很容易地向下打破系统进入大量小，集中包。

#### JavaScript的，符合C ++

与本地代码进行交互也非常简单。例如，我们写了周围的Oniguruma正则表达式引擎的包装，我们TextMate的语法支持。在浏览器中，这将需要冒险与NaCl或Esprima。节点集成使它容易。

除了节点API，我们也暴露的API的本机对话框，添加应用和上下文菜单项，操纵窗口尺寸等

#### [](https://atom.io/docs/latest/getting-started-why-atom#web-tech-the-fun-parts)网络技术：本有趣的部分

关于编写代码的Atom另一个伟大的事情是，它是在铬的最新版本上运行的保证。这意味着我们可以忽略类似浏览器的兼容性和polyfills问题。我们可以使用的明天，今天的所有网页的光泽特性。

例如，我们的工作空间和面板的布局是基于flexbox。这是一个新兴的标准，并通过大量的变化已经从我们开始使用它，但只要没有要紧，因为它的工作。

随着整个行业的推动网络技术向前发展，我们有信心，我们正在构建原子在肥沃的土壤。原生UI技术来来去去，但Web是一种标准，变得更强大和无处不在的，每过一年。我们很高兴能深入挖掘它的工具箱。

### [](https://atom.io/docs/latest/getting-started-why-atom#an-open-source-text-editor)一个开源的文本编辑器

我们看到原子作为一个完美的补充，以GitHub的主要共同努力建设更好的软件的使命。Atom是一个长期的投资，而GitHub上会继续支持其发展有一个专门的团队前进。但我们也知道，我们不能达到我们的愿景凌孤单。由于Emacs和Vim已经证实，在过去三十年里，如果你想建立一个繁荣，持久的社区围绕一个文本编辑器，它是开源的。

整个凌编辑器是免费的，开源和下可[_https://github.com/atom_](https://github.com/atom)组织。

## 安装的Atom

要开始使用的Atom，我们需要得到它在我们的系统。本节将投奔在Mac，Windows和Linux，以及如何从源代码建立它的基础上安装的Atom。

安装的Atom应该在这些系统中相当简单。一般来说，你可以简单地去[_https://atom.io_](https://atom.io/)，并在页面的顶部，你会看到一个下载按钮在[图1-1](https://atom.io/docs/latest/ch00/_download_button)。

![下载按钮](https://atom-test.s3-us-west-2.amazonaws.com/docs/images/c9/c97d2191966c9e6d32ae5204e2b26b2365b31c56/linux-downloads.png)

在atom.io下载按钮

该按钮应具体到你的平台，轻松地安装。然而，让我们对他们在这里有点细节。

### [](https://atom.io/docs/latest/getting-started-installing-atom#atom-on-mac)原子在Mac

原子最初是专为Mac和应该是一个简单的安装过程。您可以从atom.io网站打的下载按钮，或者你可以去到了Atom发布页面：

[_https://github.com/atom/atom/releases/latest_](https://github.com/atom/atom/releases/latest)

在这里，您可以下载`atom-mac.zip`明确的文件。

一旦你有了这个文件，你可以点击它来提取二进制，然后将新`的Atom`应用程序到您的“应用程序”文件夹中。

我们还建议你运行“窗口：安装Shell命令”从[命令面板](https://atom.io/docs/latest/getting-started-atom-basics#command-palette)，让您可以使用`原子`和`APM`的命令，从终端。

### [](https://atom.io/docs/latest/getting-started-installing-atom#atom-on-windows)原子在Windows

原子带有一个Windows安装程序。您可以从下载安装程序[_https://atom.io_](https://atom.io/)或：

[_https://github.com/atom/atom/releases/latest_](https://github.com/atom/atom/releases/latest)

这将安 ​​装的Atom，添加`原子`和`APM`命令你的`PATH`，在桌面上，并在开始菜单创建快捷方式，也可以增加一个公开赛在资源管理器中的Atom上下文菜单。

![原子在Windows](https://atom-test.s3-us-west-2.amazonaws.com/docs/images/14/14815cb86cc7c69fdaa574391bdaa96b43d51ea5/windows.gif)

原子在Windows

如果你只是想下载一个`.ZIP`最新的Atom版本的Windows，你也可以把它从[凌动版本页面](https://github.com/atom/atom/releases)的[_https://github.com/atom/atom/releases_](https://github.com/atom/atom/releases)。

### [](https://atom.io/docs/latest/getting-started-installing-atom#atom-on-linux)原子上的Linux

要安装的Atom在Linux上，你可以下载一个[Debian软件包](https://atom.io/download/deb)或[RPM包](https://atom.io/download/rpm)无论是从[主要的Atom网站](https://atom.io/)在atom.io或从Atom项目发布页面[_https://github.com/atom/atom/releases_](https://github.com/atom/atom/releases)。

在Debian，你会安装Debian的包`dpkg -i来`：
    
    $ sudo的dpkg -i来原子amd64.deb
    

在RedHat或其他基于RPM的系统，你可以使用`转-i`命令：
    
    $转-i atom.x86_64.rpm
    

### [](https://atom.io/docs/latest/getting-started-installing-atom#atom-from-source)从来源原子

如果没有这些选项为你工作，或者你只是想从源代码编译的Atom，你也可以做到这一点。

有详细和最新打造的Mac，Windows，Linux和FreeBSD的指令在：[_https://github.com/atom/atom/tree/master/docs/build-instructions_](https://github.com/atom/atom/tree/master/docs/build-instructions)

## 基础知识

现在的Atom安装在系统上，让我们的火起来，配置和结识的编辑器。

当您启动凌动第一次，你应该得到的屏幕，看起来像这样：

![原子欢迎屏幕](https://atom-test.s3-us-west-2.amazonaws.com/docs/images/e5/e52aa597888daf917f9f17b0b4128fb9b0982771/first-launch.png)

Atom的欢迎屏幕

这是Atom欢迎屏幕，给你一个很好的起点，如何开始与编辑。

### [](https://atom.io/docs/latest/getting-started-atom-basics#basic-terminology)基本术语

首先，让我们熟悉了一些，我们将使用本手册中的术语。

缓冲

缓冲区是在Atom中文件的文本内容。它基本上是一样的大部分描述文件，但它的原子有内存的版本。举例来说，你可以改变一个缓冲的文本，它不会被写入它相关的文件，直到你保存它。

窗格

窗格是凌动的视觉部分。如果你看一下我们刚刚推出的欢迎屏幕上，你可以看到四个窗格 - 标签栏，排水沟（已在这行号），在底部的状态栏，最后的文本编辑器。

### [](https://atom.io/docs/latest/getting-started-atom-basics#command-palette)命令面板

在欢迎屏幕中，我们介绍了可能在Atom中，“命令面板”中最重要的命令。如果你打`CMD移-P `，而专注在编辑器窗格中，命令面板会弹出。

在整本书中，我们将使用快捷键绑定像`CMD移-P`来演示如何运行一个命令。这是默认的键绑定的原子在Mac上。他们可能偶尔会略有不同，这取决于你的平台上。

您可以使用命令面板来查找正确的键绑定，如果它不出于某种原因。

该搜索驱动菜单可以做几乎任何重大的任务是可能的原子。相反一下周围所有的应用程序菜单寻找的东西，你可以打`CMD移-P`和搜索命令。

![命令面板](https://atom-test.s3-us-west-2.amazonaws.com/docs/images/fa/fa1c04ca7080cdc09ee1784b94c3e8eac4cd24da/command-palette.png)

命令面板

你不仅可以看到并迅速通过搜索成​​千上万的可能的命令，但你也可以看看是否有与之关联的键绑定。这是伟大的，因为它意味着你能猜到自己的方式做有趣的事情，同时也是学习的快捷键笔画做。

对于本书的其余部分，我们会尽量清楚你可以在命令面板中搜索除了键绑定不同的命令文本。

### [](https://atom.io/docs/latest/getting-started-atom-basics#settings-and-preferences)设置和偏好

原子有许多设置和偏好，你可以修改它的设置屏幕上。

![Atom的设置画面](https://atom-test.s3-us-west-2.amazonaws.com/docs/images/a9/a9d42c222312bdff26799a07e1ad4861f78b8441/settings.png)

Atom的设置画面

这包括诸如更改配色方案或主题，指定如何处理包装，字体设置，标签大小，滚动速度等等。您还可以使用该屏幕来安装新的包和主题，其中我们将在[“凌动包”](https://atom.io/docs/latest/ch02/_atom_packages)。

要打开设置界面，你可以去_首选项_菜单项下的菜单栏中的主要的“凌动”菜单。您也可以搜索`设置视图：开`在命令面板或使用`CMD-，`键绑定。

#### [](https://atom.io/docs/latest/getting-started-atom-basics#changing-the-color-theme)更改颜色主题

设置视图，您还可以改变颜色主题的Atom。原子附带4种不同的UI颜色主题，凌动的黑暗与光明的变种和一个主题，以及8种不同的语法颜色主题。您可以修改活动的主题或通过单击“主题”菜单项中设置视图的侧边栏安装新的主题。

![主题设置](https://atom-test.s3-us-west-2.amazonaws.com/docs/images/c4/c4a2eb1e5df49898661d1f6c86bba9074928cb78/theme.png)

改变从设置主题

在UI主题修改，如标签和树视图UI元素的颜色，而语法主题修改文字的语法高亮加载到编辑器。要更改主题，简单收拾东西的下拉列表不同。

也有几十个主题上Atom.io，你可以从你想要的东西不同的选择。我们也将涵盖定制的主题[???](https://atom.io/docs/latest/ch00/_customizing_themes)并创造自己的主题[???](https://atom.io/docs/latest/ch00/_creating_themes)。

#### [](https://atom.io/docs/latest/getting-started-atom-basics#soft-wrap)柔软的包裹

您也可以使用设置查看到指定空格和包装的偏好。

![主题设置](https://atom-test.s3-us-west-2.amazonaws.com/docs/images/f9/f9789fda13e322856108013d7b5e1c655d4c9b8d/settings-wrap.png)

改变从设置主题

当你到了启用“软标签”将插入空格，而不是实际的制表符`标签`键和“标签长度”指定多少空间，当你这样做的插入，或者有多少位来表示一个标签，就好像“软标签”被禁用。

“软换行”选项将换行太长以适应当前窗口。如果软性包装被禁止，该线将只需运行关闭屏幕的一侧，你将不得不滚动窗口看到的内容的其余部分。如果“软包裹在优先线路长度”被触发，该线将包裹在80个字符，而不是屏幕的结束。您还可以更改默认的行长度为大于80此屏幕上的其它。

在[“基本定制”](https://atom.io/docs/latest/ch02/_basic_customization)，我们将看到如何设置不同包装的偏好不同类型的文件（例如，如果你想换降价文件，但没有代码文件）。

#### [](https://atom.io/docs/latest/getting-started-atom-basics#beta-features)测试功能

由于凌动开发，但是也有一些测试，他们mainlined为大家面前偶尔的新功能。在某些情况下，被运往这些更改默认关闭的，但是可以在设置视图中启用如果您想尝试一下。

![在设置测试版功能查看](https://atom-test.s3-us-west-2.amazonaws.com/docs/images/f5/f5283c5926e9a8a52abaeb9aaf8d6510a1f97dc4/advanced-settings.png)

在设置测试版功能查看

这主要是有用的包装开发人员可以访问某个功能或之前将其更改船舶向一般人群扩散，以确保其包装仍与新功能的工作原理。但是，它可能是有趣的尝试一些这些功能了偶尔，如果你感兴趣的是即将到来。

### [](https://atom.io/docs/latest/getting-started-atom-basics#opening-modifying-and-saving-files)打开，修改和保存文件

现在，你的编辑器是寻找和表演你怎么想，让我们开始开放和编辑文件。这毕竟是一个文本编辑器，对不对？

#### [](https://atom.io/docs/latest/getting-started-atom-basics#opening-a-file)打开文件

有几种方法来打开在原子的一个文件。您可以通过选择菜单栏中的“文件>>打开”，或按做`CMD-O`可供选择的系统对话框的文件。

![打开文件](https://atom-test.s3-us-west-2.amazonaws.com/docs/images/ca/cacec139f0009157114f93a25ce7174e5d66ebbf/open-file.png)

通过对话框打开文件

这是（对，明年更多）在打开未包含在项目你当前的文件非常有用，或者如果你是从出于某种原因一个新的窗口启动。

另一种方式来打开原子的文件是通过命令行。在Atom菜单栏上有一个名为“安装Shell命令”，这在你的终端被称为安装了一个新的命令命令`原子`。您可以与一个或多个文件路径运行此开拓这些文件中的Atom。
    
    $原子-h
    原子编辑v0.152.0
    
    用法：原子[选项] [路径...]
    
    一个或多个路径，以文件或文件夹可以被指定。如果有一个
    包含所有给定的文件夹，路径现有的Atom窗口
    将在该窗口中打开。否则，他们将在新的开放
    窗口。
    
    ...
    

这是一个伟大的工具，如果你使用的终端，或者您从终端很多工作。刚刚火过`原子[文件]`，您就可以开始编辑。

#### [](https://atom.io/docs/latest/getting-started-atom-basics#editing-and-saving-a-file)编辑和保存文件

编辑文件是非常简单的。您可以点击周围，滚动使用鼠标并输入更改内容。没有特殊的编辑模式或键命令。

保存文件，你可以从菜单栏或选择“文件>>保存” `CMD-S`来保存文件。如果选择“另存为”或按`CMD移-S `，那么你可以保存你的编辑器的当前内容在不同的文件名 ​​。最后，你可以选择`CTL移-S`保存在Atom中所有打开的文件。

### [](https://atom.io/docs/latest/getting-started-atom-basics#opening-directories)打开目录

原子并不仅仅与单个文件虽然工作; 你很可能会花大部分的时间在多个文件的项目。要打开一个目录，选择菜单栏中的“文件>>打开”，然后从对话框中的目录。您还可以添加多个目录，以你目前的Atom窗口，从菜单栏中选择“文件>>添加项目文件夹...”或者按`CMD移-O `。

你可以通过它们的路径到打开任意数量的命令行目录的`原子`命令行工具。例如，您可以运行命令`原子./hopes ./dreams`打开双方`的希望`和`梦想`，同时目录。

当您打开原子与一个或多个目录，您将自动获得你的窗口一侧的树视图。

![打开一个项目](https://atom-test.s3-us-west-2.amazonaws.com/docs/images/77/77ee18071ecf6381732df2fc80fb6f2968796295/project-view.png)

在一个开放的项目树视图

树视图允许你去探索和修改项目的文件和目录结构。您可以打开，重命名，删除，并从该视图中创建新的文件。

您也可以隐藏和显示其与`CMD- \`或`树视图：切换`从调色板命令，`CTRL-0`将重点吧。当树视图具有焦点，你可以按`一`，`米`或`删除`添加，移动或删除文件和文 ​​件夹。你也可以简单地在树视图中的文件或文件夹，单击右键看到许多不同的选项，其中包括所有这些加显示在您的本地文件系统中的文件或复制文件路径到系统剪贴板。

## 原子模块

比如Atom的许多地方，树的观点并没有直接内置到编辑器，但它是简单地随凌默认自己的独立包。

你可以在这里找到源代码树视图：[_https://github.com/atom/tree-view_](https://github.com/atom/tree-view)

这是关于Atom的有趣的事情之一。许多它的核心功能实际上只是包实现，你会实现任何其他功能一样。这意味着，如果你不喜欢，例如树视图，这是相当简单的编写自己实现这些功能，并完全替代它。

#### [](https://atom.io/docs/latest/getting-started-atom-basics#opening-a-file-in-a-project)打开文件的项目

一旦你有一个项目的Atom开放的，你可以很容易地找到和项目中打开的任何文件。

如果碰到任何`CMD-T`或`CMD-P `，模糊查找对话框会弹出。这将让你快速搜索所有文件中的所有目录中的项目通过键入路径的部分。

![打开一个项目](https://atom-test.s3-us-west-2.amazonaws.com/docs/images/30/30db3bd19e647bd1675ecfab1647927ea8c78416/finder.png)

打开文件模糊搜索

您也可以只通过当前打开的（而不是在项目中的每个文件）的文件中搜索`CMD-B `。该搜索通过您的“缓冲区”或打开文件。您也可以限制这种模糊搜索`CMD移-B `，它搜索只能通过它们是新的或已被修改自上次的Git提交的文件。

模糊取景同时使用`core.ignoredNames`和`模糊finder.ignoredNames`配置设置来过滤出的文件和文 ​​件夹，将不被显示。如果你有万吨文件的项目，你不希望它进行搜索，您可以添加模式或路径，其中任一配置设置。我们将学习更多关于配置设置[???](https://atom.io/docs/latest/ch00/_config_settings)，但现在你可以很容易地设置这些在设置查看核心设置下。

作为由minimatch Node.js的库实现这两方面的配置设置被解释为glob模式。

你可以阅读更多关于minimatch这里：[_https://github.com/isaacs/minimatch_](https://github.com/isaacs/minimatch)

这个包也还没有显示的Git忽略的文件时，`core.excludeVcsIgnoredPaths`启用。您可以轻松地在设置视图切换此，它的顶部的选项之一。

## 总结

你现在应该有一个基本的了解什么Atom是，你想用它做什么。你也应该有它安装在系统上，并能够使用它的最基本的文本编辑操作。

现在，你就可以开始挖掘到有趣的东西。

# 使用ATOM

现在，我们已经介绍的Atom非常基础，我们已经准备好，看看如何真正开始得到最有效地使用它。在本章中，我们将看看如何找到并且为了安装新的软件包中添加新的功能，如何找到并安装新的主题，如何使用和更先进的方式处理文本，如何自定义在任意编辑器这样，你想，如何使用Git工作进行版本控制等。

## 原子包

首先，我们将开始与凌包装系统。正如我们前面所提到的，凌动本身就是功能非常基本的核心附带了一些像添加新功能有用的包[树视图](https://github.com/atom/tree-view)和[设置视图](https://github.com/atom/settings-view)。

事实上，有超过70包包括所有可用的凌动默认功能。正如一些例子中，[欢迎对话框](https://github.com/atom/welcome)，你看，当你第一次启动时，[拼写检查](https://github.com/atom/spell-check)，在[主题](https://github.com/atom/atom-dark-ui)和[模糊的取景器](https://github.com/atom/fuzzy-finder)是分开保存所有的包和所有使用您可以访问相同的API，因为我们会看到很详细的[???](https://atom.io/docs/latest/ch00/_hacking_atom)。

这意味着，包可以是非常强大的，并且可以改变一切从非常外表整个界面和感觉到的甚至核心功能的基本操作。

为了安装一个新的软件包，您可以使用软件包选项卡，在熟悉的设置视图。只需打开设置视图（`CMD-， `），点击“软件包”选项卡上，然后键入您的搜索查询框下的安装包提示“搜索包”。

这里列出的包已经发布到[atom.io](https://atom.io/packages)这是凌动包正式登记。搜索上的设置面板中会去atom.io包注册表和拉在任何符合您的搜索条件。

![包安装界面](https://atom-test.s3-us-west-2.amazonaws.com/docs/images/d4/d4afb76746849869cfa3a11dbd3c03049e3db906/packages.png)

包安装界面

所有的软件包将拿出一个“Install”按钮。点击将下载包并安装它和你的编辑器现在将开始有此功能。

### [](https://atom.io/docs/latest/using-atom-atom-packages#package-settings)套餐设置

一旦软件包安装在Atom中，它会显示在你的设置屏幕的侧边栏，以及所有预装包附带的Atom。要过滤，以找到一个列表中，您可以键入“包过滤”文本框。

![套餐设置屏幕](https://atom-test.s3-us-west-2.amazonaws.com/docs/images/66/6670713ef458a8418aa83196abe106d34b3f7ee1/package-settings.png)

套餐设置屏幕

点击的软件包名称之一会给你的设置屏幕包。在这里，你必须改变一些默认变量包的选项，看到的所有的命令键绑定的，禁止包暂时，查看源代码，看到包的当前版本，报告问题和卸载包。

如果您的任何软件包的新版本发布时，原子会自动检测到它，你可以从该屏幕或从主包中的搜索选项卡升级包。这可以帮助你轻松保持你的所有已安装的软件包保持最新。

### [](https://atom.io/docs/latest/using-atom-atom-packages#atom-themes)原子主题

您还可以找到从设置视图安装新的主题的Atom。这些可以是UI主题或语法高亮主题，你可以搜索他们的“主题”选项卡，就像寻找新的软件包。

![主题搜索屏幕](https://atom-test.s3-us-west-2.amazonaws.com/docs/images/5e/5e29af167aa4a96ff3b715e0d18351c1500bdb14/themes.png)

主题搜索屏幕

点击任何主题的“了解更多”按钮，将带你到上atom.io为主题的个人资料页面那里几乎总是一个截图看到什么主题的样子。

点击“安装”，将安装主题，并使其在主题的下拉列表中可以作为我们看到了 [“改变颜色的主题”](https://atom.io/docs/latest/ch01/_color_themes)。

![主题搜索屏幕](https://atom-test.s3-us-west-2.amazonaws.com/docs/images/e0/e0410c2e9b8b06dd4dcce90e4bd1a343cd96d95d/unity-theme.png)

的统一UI主题与Monokai语法主题的例子

### [](https://atom.io/docs/latest/using-atom-atom-packages#command-line)命令行

您也可以在命令行中使用安装软件包或主题`APM`。

检查是否已`APM`运行在终端下面的命令安装：
    
    $ apm help install
    

您应该看到一条消息，打印出带有一些细节`APM安装`命令。

如果你不这样做，推出Atom和运行_的Atom>安装Shell命令_菜单安装`APM`和`原子`命令。

您也可以通过使用安装软件包`安装APM`命令：

  * `apm install <package_name>`安装最新版本。

  * `apm install <package_name>@<package_version>`安装特定版本。

例如`APM安装emmet@0.1.5`安装`0.1.5`版本的[埃米特](https://github.com/atom/emmet)包。

您还可以使用`APM`寻找新的软件包安装。如果你运行`APM的搜索`，可以搜索包注册表中搜索词。
    
    $ APM搜索咖啡
    搜索结果对于“咖啡”（5）
    ├──咖啡迹加入智能跟踪语句咖啡文件每一个按键。（77下载，3星级）
    ├──咖啡导航代码导航面板咖啡脚本（557下载，8星）
    ├──原子编译咖啡这Atom.io包编译.coffee上的文件保存到.js文件。（myJavascript.coffee  - > myJavascript.js）（349下载，4星）
    ├──咖啡皮棉的CoffeeScript棉短绒（3336下载，18星）
    └──在原子编辑混帐的grep'混帐grep`（1224下载，9星）
    
    
    $ apm search coffee
    Search Results For 'coffee' (5)
    ├── coffee-trace Add smart trace statements to coffee files with one keypress each. (77 downloads, 3 stars)
    ├── coffee-navigator Code navigation panel for Coffee Script (557 downloads, 8 stars)
    ├── atom-compile-coffee This Atom.io Package compiles .coffee Files on save to .js files. (myJavascript.coffee -> myJavascript.js) (349 downloads, 4 stars)
    ├── coffee-lint CoffeeScript linter (3336 downloads, 18 stars)
    └── git-grep `git grep` in atom editor (1224 downloads, 9 stars)
    

您可以使用`APM视图`以查看有关特定包的详细信息。
    
    $ APM观点混帐的grep
    混帐的grep
    ├──0.7.0
    ├──混帐：//github.com/mizchi/atom-git-grep
    在原子编辑├──'混帐grep`
    ├──1224下载
    └──9星
    
    运行`APM安装混帐grep`安装该软件包。
    
    
    $ apm view git-grep
    git-grep
    ├── 0.7.0
    ├── git://github.com/mizchi/atom-git-grep
    ├── `git grep` in atom editor
    ├── 1224 downloads
    └── 9 stars
    
    Run `apm install git-grep` to install this package.
    

## 朝着凌

虽然它很容易通过点击鼠标或使用箭头键移动的Atom，有一些按键绑定，可以帮助你保持你的双手在键盘上和浏览周围的快一点。

首先，凌附带了许多基本的Emacs键绑定用于导航文档。去向上和向下一个字符，你可以使用`CTRL-P`和`CTRL-N `。走左，右一个字符，你可以使用`CTRL-B`和`CTRL-F `。这些都是使用箭头键，虽然有些人喜欢没有把他们的手到方向键位于键盘上的等价物。

除了单个字符的运动，还有一些其他的运动键绑定。

`ALT-B`，`ALT-左`

移动到单词的开头

`ALT-F`，`ALT-权`

移动到单词的末尾

`CMD-右`，`CTRL-E`

移动到行尾

`CMD-离开`，`CTRL-A`

移动到行的第一个字符

`CMD-了`

移动到文件的顶部

`CMD下`

移动到文件底部

您也可以直接移动到指定的行（和列）的数量与`CTRL-G `。这将弹出，询问你这行想跳到一个对话框。还可以使用的`行：列`语法跳转到一个字符在该行的为好。

![前往路线](https://atom-test.s3-us-west-2.amazonaws.com/docs/images/5c/5cc297d4928cb9beeeb1b2f3aed3dea0006ac29e/goto.png)

直接去线

### [](https://atom.io/docs/latest/using-atom-moving-in-atom#navigating-by-symbols)通过符号浏览

您也可以围绕多一点informatively跳。要跳转到一个符号，如方法定义，按`CMD-R `。这将打开当前文件中的所有符号，则可以模糊滤镜类似于其中的列表`CMD-吨`。要搜索整个项目的符号，使用`CMD-Shift-R键`。

![通过在你的项目符号搜索](https://atom-test.s3-us-west-2.amazonaws.com/docs/images/65/65bee03770c49c4e5b51cfb5e836407331e669a7/symbol.png)

通过在你的项目符号搜索

您还可以使用`CTRL-ALT-下`直接跳转到光标下的方法或函数的声明。

首先，你需要确保你有`标签`（或`标签`）为您的项目生成的文件。这可以通过安装完成[的ctags](http://ctags.sourceforge.net/)并运行一个命令，如`CTAGS -R的src /`从你的项目的根目录下的命令行。

如果你是一个Mac上使用[自制软件](http://brew.sh/)，你可以运行`BREW安装的ctags`。

您可以自定义标签是如何通过创建自己产生`.ctags`文件在你的home目录（`〜/ .ctags`）。一个例子可以找到[这里](https://github.com/atom/symbols-view/blob/master/lib/.ctags)。

符号导航功能在实施[原子/符号视图](https://github.com/atom/symbols-view)封装。

### [](https://atom.io/docs/latest/using-atom-moving-in-atom#atom-bookmarks)原子书签

原子也有一个伟大的方式来书签具体线路在您的项目，所以你可以跳回到他们迅速。

如果按`CMD-F2`，凌动将切换当前行一个“书签”。您可以设置这些整个项目，并利用它们来快速查找和跳转到你的项目的重要线路。一个小的书签符号被添加到线沟，类似于在73线[图2-7](https://atom.io/docs/latest/ch00/_bookmarks_image)。

如果你打`F2`，凌会跳转到下一个书签文件中，你目前的重点。如果使用`移F2`它将向后循环通过它们来代替。

您还可以看到所有的项目目前的书签列表，并迅速筛选它们，并跳转到其中的任何击中`CTRL-F2`。

![书签](https://atom-test.s3-us-west-2.amazonaws.com/docs/images/e7/e7c453a3376224b2042fd7fa617c522f87c01f66/bookmarks.png)

查看和过滤器的书签。

所述书签功能是在实现[原子/书签](https://github.com/atom/bookmarks)包。

## 原子选择

选择在Atom中文字的范围可以是一些有用的东西。它可以是范围界定某些操作，如删除，搜索或缩进。它也可以是喜欢的事情或引用包围文本有帮助的。

选择镜像很多运动命令。它们实际上是完全相同的键绑定作为移动的命令，但与一`移`中加入键。

`Ctrl-Shift组合-P`

最多选择

`按Ctrl-Shift-N键`

选择向下

`Ctrl-Shift组合-B`

选择前一个字符

`按Ctrl-Shift-F组合`

选择下一个字符

`ALT移-B `，`ALT-左移位`

选择单词的开头

`ALT移-F `，`ALT移权`

选择单词的结束

`Ctrl-Shift组合-E`，`CMD移权`

选择线的结束

`Ctrl-Shift组合-A`，`CMD移左`

选择行的第一个字符

`CMD-升档`

选择文件的顶部

`CMD-降档`

选择到文件底部

除了光标移动选择命令，也有一些命令，帮助与选择的内容的具体领域。

`CMD-A`

选择整个缓冲区

`CMD-L`

选择整条生产线

`Ctrl-Shift组合-W`

选择当前字

## 编辑和删除文本

到目前为止，我们已经看了很多方法可以走动，并选择一个文件的地区，所以现在让真正改变一些文字。很明显，你可以输入为了插入字符，但也有一些方法可以删除和处理文本，可以派上用场。

### [](https://atom.io/docs/v0.191.0/using-atom-editing-and-deleting-text#basic-manipulation)基本操作

也有少数的酷键绑定的基本文本操作，可能派上用场。这些范围从走动文本行，复制线改变的情况下。

`CTRL-T`

转字符。此交换上的光标的任一侧的两个字符。

`CMD-J`

加入下一行到当前行的结尾

`CTRL-CMD-了`，`CTRL-CMD下`

移动当前行向上或向​​下

`CMD-移-D-`

重复当前行

`CMD-K，CMD-U`

上壳体当前字

`CMD-K，CMD-L`

小写当前字

原子还具有内置的功能，在给定的最大行长度重新流向一个段落硬包装。您可以格式化当前选择到不超过80个（或任何号码都行`editor.preferredLineLength`使用设置为）字符`CMD-ALT-Q `。如果没有选择，当前段落将回流。

### [](https://atom.io/docs/v0.191.0/using-atom-editing-and-deleting-text#deleting-and-cutting)删除和切割

您也可以删除或剪切文本进行了一些快捷键的缓冲区。要狠。

`Ctrl-Shift组合-K`

删除当前行

`CMD-删除`

删除到行尾（`CMD-FN-退格`在Mac上）

`CTRL-K`

剪线结束

`CMD-退格`

删除行首

`ALT-退格键`，`ALT-H`

删除到单词的开头

`Alt删除`，`ALT-D`

删除字的结束

### [](https://atom.io/docs/v0.191.0/using-atom-editing-and-deleting-text#multiple-cursors-and-selections)多个游标和选择

其中一个很酷的事情，凌能做到开箱即用的是支持多个游标。这可能是在处理文本的一长串难以置信的帮助。

`CMD点击`

添加新的光标

`CMD-移-L-`

转换一个多线路选择到多个游标

`CTRL移了`，`CTRL-升档`

添加另一个光标上方/当前光标下方

`CMD-D`

选择下一个词的文档中的是一样的当前所选词

`CTRL-CMD-G`

选择文档的相同的当前光标下的一（多个）的所有单词

使用这些命令，你可以把光标在文档中的多个地方，并有效地同时执行多个位置相同的命令。

![使用多个游标](https://atom-test.s3-us-west-2.amazonaws.com/docs/images/5d/5dceacf4319ebd1026ac543f95156f8c8c111636/multiple-cursors.gif)

使用多个游标

这可能是在做许多类型的重复任务，如重命名变量或改变一些文本的格式难以置信的帮助。您可以使用此与几乎任何插件或命令 - 例如，改变外壳和移动或复制行。

您也可以使用鼠标选择文本的`命令，`按下可同时选择文本的多个区域的关键。

### [](https://atom.io/docs/v0.191.0/using-atom-editing-and-deleting-text#whitespace)空白

原子带有一对夫妇的工具来帮助你管理你的文档中的空白。这些工具中的实现[原子/空白](https://github.com/atom/whitespace)包。

第一个是转换前导空格，以标签和命令相当于改变卡口插入空格。如果您正在使用具有混合空白文档，这些命令可能是巨大的帮助正常化文件。有没有键绑定这些，所以你将不得不寻找你的命令调色板“转换为空间标签”（反之亦然）来运行这些命令之一。

空白的辅助工具，保持作为一个单独的封装，因此对于它的设置可以在该页面管理`的空白`包。

![空白的设置](https://atom-test.s3-us-west-2.amazonaws.com/docs/images/a2/a2bea5893c0008794fbfadd473b344d07b1ce8ad/whitespace.png)

管理您的空白设置

请注意，“删除尾随空白”选项默认是打开的。这意味着，每次你保存的Atom打开任何文件时，它将剥离从文件中所有尾随空白。如果你想关闭这个功能，进入到`空白`包在你的设置面板，并取消选中该选项。

原子也将在默认情况下确保您的文件有一个尾随的换行符。您还可以禁用该屏幕上这个选项。

### [](https://atom.io/docs/v0.191.0/using-atom-editing-and-deleting-text#brackets)括号

原子附带的智能和易于使用的支架搬运。

它会默认高亮显示[]，（）和{}风格托架，当你的光标超过他们。它还将突出匹配XML和HTML标签。

原子也将自动自动完成[]，（）和{}，“”，“”，“”，“”，«»，<>，当你键入的佼佼者反引号。如果你有一个选择，你键入任何这些开放括号或引号，凌会附上开幕和闭幕括号或报价的选择。

有迹象表明，你可以用一些其他有趣的支架相关的命令。

`CTRL-M`

跳转到托架匹配所述一个相邻的光标。它会跳转到最近的封闭支架时，有没有相邻支架。

`CTRL-CMD-M`

选择所有当前括号内的文字

`ALT-CMD-。`

关闭当前XML / HTML标记

支架的功能是在实现[原子/托架匹配](https://github.com/atom/bracket-matcher)包。像所有的这些包，要改变与支架违约处理，或完全禁用它，您可以导航到该包中的设置视图。

### [](https://atom.io/docs/v0.191.0/using-atom-editing-and-deleting-text#encoding)编码

原子还附带了一些基本的文件编码的支持，你应该发现自己与非UTF-8编码的文件的工作，或者如果您想创建一个。

`Ctrl-Shift组合-U`

切换菜单来更改文件编码

如果你拉起文件编码对话框，你可以选择一个备用文件编码保存在文件中。通常它会自动检测，如果它可以编码，否则将默认为UTF-8。新文件也将是UTF-8的文件默认情况下。

![文件编码](https://atom-test.s3-us-west-2.amazonaws.com/docs/images/a5/a5b6907c3ba679e012505eb3d5d62147149b5e86/encodings.png)

改变你的文件编码

如果你拉起编码菜单​​和更改当前编码到别的东西，该文件将您保存该文件的下一次写在了编码。

编码选择器的实施的[原子/编码选择器](https://github.com/atom/encoding-selector)包。

## 查找和替换

查找和你的文件或项目替换文本是快速和容易的Atom。

`CMD-F`

缓冲区内搜索

`CMD-Shift-F组合`

搜索整个的项目

如果启动任何这些命令，你将会看到的“查找和替换”面板在屏幕的底部。

![查找和替换文件](https://atom-test.s3-us-west-2.amazonaws.com/docs/images/c0/c03ae9dcc5781bed23daf8956bddf7ecce000914/find-replace-file.png)

查找与当前文件中替换文本

您当前的文件中搜索，你可以打`CMD-F `，键入搜索字符串，然后按下回车键（或`CMD-G`或“查找下一个”按钮）多次循环通过在该文件中所有的比赛。还有一些按钮来切换大小写，正则表达式匹配和选择范围界定。

如果你输入一个字符串中的“替换当前缓冲区”文本框，你可以用不同的字符串替换匹配。例如，如果你想替换字符串“斯科特”字符串“龙”的每一个实例，你会在两个文本框中输入的值，并打出了“全部替换”按钮执行替换。

如果你调用面板，您也可以做到这一点贯穿整个项目`CMD-Shift-F组合`。

![查找和替换项目](https://atom-test.s3-us-west-2.amazonaws.com/docs/images/c9/c977d802199d520792cee280756a322b27fe04ce/find-replace-project.png)

查找并在您的项目替换文本

这是一个伟大的方式，找出项目中的一个函数被调用时，锚链接或特定的拼写错误所在。点击匹配的行会跳到你在文件中的位置。

您可以通过输入一个搜索文件的一个子集在您的项目[glob模式](http://en.wikipedia.org/wiki/Glob_%28programming%29)进入“文件/目录模式”文本框中。当你有多个项目的文件夹打开的，这个功能也可以用在只有一个这些文件夹中进行搜索。例如，如果你有文件夹`/路径1 /文件夹1`和`1 /路径/ FOLDER2`开放，您可以输入开头的模式`文件夹1`只在第一个文件夹进行搜索。

打`逃生`，而专注于查找和替换窗格中清除面板从您的工作空间。

查找和替换功能，在实现[原子/查找和替换](https://github.com/atom/find-and-replace)包，并使用[原子/丑闻](https://github.com/atom/scandal)包做实际的搜索。

## 片段

片段是一个令人难以置信的强大的方式来快速生成一个快捷方式通常需要的代码语法。

我们的想法是，你可以键入类似`的habtm`然后打`标签`的关键，这将扩展到`has_and_belongs_to_many`。

很多包都捆绑了自己的片段，是特定于该模式。例如，`语言HTML`包，提供了对HTML语法高亮和语法支持来自几十个片段，创造很多你可能需要使用不同的HTML标签。如果您在原子的新的HTML文件，您可以键入`HTML`，然后打`标签`，它会扩大到：
    
    <HTML> 
      <HEAD> 
        <标题> </ title> 
      </ HEAD> 
      <BODY>
    
      </ body> 
    </ HTML>
    
    
    <html>
      <head>
        <title></title>
      </head>
      <body>
    
      </body>
    </html>
    

它也将光标定位在中间的`标题`标记，以便您可以立即开始填写标签。不少片段有多个焦点，你可以移动通过与`卡`键以及-例如，在这个HTML片段的情况下，一旦你填写的标题标签，你可以打`标签`，光标移动到中间身体标记。

要查看所有您当前已打开的文件类型的可用片段，您可以键入`ALT移-S `。

![鉴于片段](https://atom-test.s3-us-west-2.amazonaws.com/docs/images/44/44a7f1820819228863fd2ec3c497b8cee8d21555/snippets.png)

查看所有可用片段

您还可以使用模糊搜索通过输入选择框来筛选列表下来。选择其中之一将执行片段在您光标（或多个游标）。

### [](https://atom.io/docs/v0.191.0/using-atom-snippets#creating-your-own-snippets)创建自己的代码段

所以这是很酷，但如果有一些语言包不包括什么是习惯你写的代码？幸运的是，这是令人难以置信的容易添加自己的片段。

有一个在你的文本文件`〜/ .atom`称为目录`snippets.cson`包含当您启动凌动装载所有的自定义代码段。不过，你也可以很容易地打开该文件通过选择_凌动>打开你的片段_菜单。

还有一个叫做目录`〜/ .atom /片段`，您可以用多个填补`JSON`或`CSON`在片段格式的文件，如果你想组织你的片段更连贯的方式。

#### [](https://atom.io/docs/v0.191.0/using-atom-snippets#snippet-format)摘录格式

所以，让我们来看看如何写一个片段。基本摘录格式如下：
    
    “.source.js' ：
      '的console.log' ：
        '前缀' ： '登录' 
        '身体' ： '的console.log（$ {1：“撞车”}）; $ 2'
    
    
    '.source.js':
      'console.log':
        'prefix': 'log'
        'body': 'console.log(${1:"crash"});$2'
    

最外层的键是选择器，其中这些片段应被激活。确定什么，这应该是最简单的方法就是去语言包，你要添加代码片段，并寻找“范围”字符串的语言。

例如，如果我们想增加一个片段，将工作的Java文件，我们会查找`语言的Java`包在我们设置视图，我们可以看到范围`source.java`。那么顶层片断重点将是由前缀一段时间（如CSS类选择会做）。

![片段范围](https://atom-test.s3-us-west-2.amazonaws.com/docs/images/02/02a7ee36edbbdabb7f708f1cca066a5c86582e09/snippet-scope.png)

查找选择范围的一个片段

按键的下一级是片段的名称。这些用来描述在片段菜​​单更可读的方式的片段。它通常最好使用某种某种人类可读的字符串这里。

在每个片段的名称是一个`前缀`应触发片段和`身体`，当片段被触发插入。

`$`后跟一个数字是可以的，按被循环的标签停止`标签`一旦片段被触发。

上面的例子中增加了一个`记录`片段来的JavaScript，将扩大到文件。
    
    console.log("crash");
    

字符串`“崩溃”`将最初选择和按Tab键会再次将光标之后`;`

#### [](https://atom.io/docs/v0.191.0/using-atom-snippets#multi-line-snippet-body)多行代码段体

您也可以通过使用多行语法`“”，“`较大的模板：
    
    “.source.js” ：“如果，否则，如果，否则，' 
      ：
        '前缀' ： 'ieie“ 
        “ 体” ： “”，“ 
          如果（$ {1：真}）{ 
            2美元
          }否则，如果（$ {3：假的}）{ 
            4美元
          }其他{ 
            5美元
          } 
        “”“
    
    
    '.source.js':
      'if, else if, else':
        'prefix': 'ieie'
        'body': """
          if (${1:true}) {
            $2
          } else if (${3:false}) {
            $4
          } else {
            $5
          }
        """
    

正如你所期望的那样，有一个片段创建片段。如果你打开一个片段文件和类型`剪断`，然后打`标签`，你会得到插入以下文字：
    
    “.source.js' ：
      '片段名称' ：
        '前缀' ： '你好' 
        “体” ： “您好！世界”
    
    
    '.source.js':
      'Snippet Name':
        'prefix': 'hello'
        'body': 'Hello World!'
    

巴姆，只需填写坏小子了，你有自己的一个片段。只要你保存文件，凌应重新加载片段，你会立即可以尝试一下。

该片段的功能是在实现[原子/片段](https://github.com/atom/snippets)包。

## 自动完成

如果你还在寻找节省一些打字的时间，凌动还带有简单的自动完成功能。

该autocompleter可以查看和使用将在编辑器中可能的补全`CTRL空间`。

![自动完成](https://atom-test.s3-us-west-2.amazonaws.com/docs/images/97/974164d19fe0321d66c422d80217dc2cbec6d8ff/autocomplete.png)

自动完成菜单

默认情况下，完成者将期待通过当前打开的文件匹配你开始什么类型的字符串。

如果你想要更多的选项，在设置面板中的自动完成包，你可以切换设置，使autocompleter看在你所有打开的缓冲区，而不仅仅是当前文件中的字符串。

对于一个更强大的自动完成功能的解决方案，跳过交给[???](https://atom.io/docs/v0.191.0/ch00/_autocomplete_plus)包，我们覆盖[???](https://atom.io/docs/v0.191.0/ch00/_common_packages)。

自动完成功能在实现 [原子/自动完成](https://github.com/atom/autocomplete)包装。

## 折页

如果你想看看你工作的代码文件的结构概述，折叠可以成为一个有用的工具。折叠隐藏为了简化什么是在屏幕上的代码块，如功能或循环块。

您可以通过单击，当您在阴沟里将鼠标光标出现的箭头折叠的代码块。您还可以折叠和键盘与展开`ALT-CMD- [`和`ALT-CMD-]`键绑定。

![代码折叠](https://atom-test.s3-us-west-2.amazonaws.com/docs/images/52/52bd79eb72caef567555dc1182b18e438b990a64/folding.png)

代码折叠的例子

折叠的一切，用`ALT-CMD-SHIFT- {`和展开都使用`ALT-CMD-SHIFT-}`。您也可以折叠在一个特定的缩进层次与`CMD-K CMD-N `，其中N是压痕深度。

最后，你可以通过做一个选择，然后打了折的代码或文字任意部分`CTRL-ALT-CMD-F`或选择在命令面板“折叠选择”。

## 窗格

您可以使用水平或垂直分割任何编辑器窗格`CMD-K箭头`所在的箭头方向拆分窗格。一旦你有一个拆分窗格，您可以将焦点它们之间有`CMD-K CMD箭头`那里的箭头方向的重点应转向。

![窗格](https://atom-test.s3-us-west-2.amazonaws.com/docs/images/72/72df54d05fad63f9f0946505123b41f433547ee8/panes.png)

多个窗格

每个窗格都有它自己的“项目”或文件，这是由标签来表示。您可以从窗格中移动的文件通过拖动鼠标拖放它们在你想要的文件，要在窗格中窗格。

要关闭一个窗格中，关闭其所有的编辑与`CMD-W `，然后按`CMD-W`一次关闭窗格。您可以配置窗格自动关闭时，空的设置视图。

## 语法

一个缓冲器的“语法”是什么语言原子认为文件内容。语法的类型将Java或降价。我们看着这个有点当我们创造了一些片段[“片段”](https://atom.io/docs/v0.191.0/ch00/_snippets)。

如果加载了一个文件，凌做了一些工作，试图找出它是什么类型的文件。在很大程度上，这是通过看它的文件扩展名来完成（`.md`一般是降价文件等），但它也有检查的内容有点弄明白，如果它是不明确的。

如果加载了一个文件和Atom不能确定语法的文件，它会默认为_纯文本_，这是最简单的一种。如果这样做，如果它miscategorizes一个文件，或者以任何理由要更改某个文件的活动语法，就可以拉起语法选择用`Ctrl-Shift组合-L `。

![语法选择](https://atom-test.s3-us-west-2.amazonaws.com/docs/images/d6/d6cd27ef804b7c07ef495820f990644951f75692/grammar.png)

语法选择

一旦文件的语法手动更改，凌会记得，直到你把它设置回自动检测或手动选择不同的语法。

语法选择器功能在实现 [原子/语法选择](https://github.com/atom/grammar-selector)包。

## 版本控制凌动

版本控制是任何项目的一个重要方面和Atom配备了基本[的Git](http://git-scm.com/)和[GitHub上](https://github.com/)集成出炉英寸

### [](https://atom.io/docs/v0.191.0/using-atom-version-control-in-atom#checkout-head-revision)结帐HEAD修订

在`CMD-ALT-Z`键绑定检查在编辑器中的文件的最新版本。

这是一个快速的方法来放弃你所做的任何保存，上演的变化和文件恢复到在HEAD提交的版本。这在本质上是一样的运行`git的结帐HEAD - <路径>`和`混帐复位HEAD - <路径>`从该路径的命令行。

![git的结帐头](https://atom-test.s3-us-west-2.amazonaws.com/docs/images/9d/9dbafe7763621837fce08d44b3fc756932493e98/git-checkout-head.gif)

Git的检出HEAD

此命令去到撤消堆栈，所以你可以使用`CMD-Z`之后，恢复以前的内容。

### [](https://atom.io/docs/v0.191.0/using-atom-version-control-in-atom#git-status-list)Git的状态列表

原子附带模糊取景器包，它提供了`CMD-T`快速的项目，并打开文件`CMD-B`跳转到任何打开的编辑器。

该软件包还配备了`CMD移-B`会弹出所有项目中未跟踪和修改的文件列表。这些将是你在命令行中，如果您运行的git状态看到相同的文件。

![git的状态](https://atom-test.s3-us-west-2.amazonaws.com/docs/images/17/17e119c799023e8ae483960663e1b1b0b0843417/git-status.gif)

Git的状态列表

一个octicon会出现每个文件的权利让你知道它是否是未跟踪或修改。

### [](https://atom.io/docs/v0.191.0/using-atom-version-control-in-atom#commit-editor)提交编辑

原子可以作为你的Git提交的编辑器，船舶与语言的git包，它增加了语法高亮编辑提交，合并和变基信息。

![混帐消息](https://atom-test.s3-us-west-2.amazonaws.com/docs/images/0f/0f36802b57ec5aea7580a70e60e6aa2216bb8eb4/git-message.gif)

Git的提交信息突出

您可以配置凌动是你的Git提交编辑器使用以下命令：
    
    $ git的配置--global core.editor “原子--wait”
    

该[语言的git](https://github.com/atom/language-git)包将帮助您用简短提交着色消息的第一线，他们是长于50和65个字符的时候。

### [](https://atom.io/docs/v0.191.0/using-atom-version-control-in-atom#status-bar-icons)状态栏图标

在[状态栏](https://github.com/atom/language-git)包附带的Atom包括若干可显示在右侧的状态栏的Git的装饰品。

![状态栏](https://atom-test.s3-us-west-2.amazonaws.com/docs/images/0d/0db63ce2f4e88eb2449d2021e9d426f9bfe299b1/git-status-bar.png)

Git的状态栏

目前已签出的分支名称显示与提交的分支或落后于它的上游分支提前数。

还一个图标被添加如果该文件是未跟踪，修改或忽略。添加的行数和删除，因为该文件被最后提交的将被显示出来。

### [](https://atom.io/docs/v0.191.0/using-atom-version-control-in-atom#line-diffs)行diff文件

所包含[的git-DIFF](https://github.com/atom/git-diff)包着色的旁边已添加，编辑，删除和线条的排水沟。

![混帐行diff文件](https://atom-test.s3-us-west-2.amazonaws.com/docs/images/b9/b99cc90d08afebd0caa32cdc8a448d249462a80d/git-lines.png)

Git的diff文件行

这个包还增加了`ALT-G下降`和`ALT-G高达`键绑定，使您可以将光标移动到下一个/上差异猛男在当前编辑器。

### [](https://atom.io/docs/v0.191.0/using-atom-version-control-in-atom#open-on-github)打开GitHub上

如果你正在从事的项目是在GitHub上，也有可以使用一些非常有用的集成。大多数命令会把你正在查看当前文件并打开在GitHub上该文件的视图 - 例如，怪或提交该文件的历史记录。

`ALT-GØ`

在GitHub上打开文件

`ALT-G B`

文件在GitHub上公开指责

`ALT-Għ`

文件在GitHub上公开赛历史

`ALT-GÇ`

复制在GitHub上当前文件的URL

`ALT-Gř`

在GitHub上的分支比较

分支比较简单说明你是对你目前工作的地方是不是在主线分支的分支提交。

![在GitHub上公开](https://atom-test.s3-us-west-2.amazonaws.com/docs/images/ea/eaade004342a5d04b347a1a7e5d842761dd1961d/open-on-github.png)

文件在GitHub上公开惹的祸

## 写的Atom

虽然它可能是最普遍的是使用原子编写软件代码，原子也可以被用来相当有效写散文。通常的做法就是在某种标记语言，如降价或做把AsciiDoc（本手册是用）。在这里，我们将迅速覆盖几个原子为帮助你写散文的工具。

在这里，我们将集中精力写作降价，但其他散文的标记语言，比如有把AsciiDoc包提供类似的功能。

### [](https://atom.io/docs/v0.191.0/using-atom-writing-in-atom#spell-checking)拼写检查

如果您在文本正在（包括纯文本文件，GitHub的降价和Git提交默认消息），原子会自动尝试检查拼写。

任何拼写错误的单词会高亮显示（默认字下方的红色虚线），你可以通过点击拉起的可能修正菜单`CMD-： `（或从右键单击上下文菜单或选择“正确的拼写”命令面板）。

![拼写检查](https://atom-test.s3-us-west-2.amazonaws.com/docs/images/ce/cec92a7cc76cbef20827a31fcf95225bef9a1a6e/spellcheck.png)

检查拼写

要添加更多的文件类型，以什么样的Atom将尝试拼写检查列表，请访问拼写检查包设置在设置视图，并添加要拼写检查的任何语法。

默认情况下，它被设置为“text.plain，source.gfm，text.git提交”，但您可以添加类似“source.asciidoc”如果你想查看这些类型的文件了。

凌动拼写检查器使用系统字典，所以如果你想它来检查拼写的另一种语言或语言环境，你可以轻松地改变它。

![拼写检查字典](https://atom-test.s3-us-west-2.amazonaws.com/docs/images/7f/7f3643e97b2d22c5caa3e7571d3d3c93e1a5f355/dictionary.png)

改变你的拼写检查字典

拼写检查是在实现[原子/拼写检查](https://github.com/atom/spell-check)包。

### [](https://atom.io/docs/v0.191.0/using-atom-writing-in-atom#previews)预览

当一个标记语言编写的散文，它往往是非常有用得到的内容将是什么时，它呈现像一个想法。原子附带了降价预览插件默认。

`CNTL移-M的`

将切换预览模式的降价。

![预览散文](https://atom-test.s3-us-west-2.amazonaws.com/docs/images/bd/bd2121bbb8e62cdfd32b463c4fe6f362fa8e1fa4/preview.png)

预览您的散文

当你编辑文本，预览也将默认更新。这使得它很容易为​​你键入时检查你的语法。

您也可以复制在预览窗格中呈现的HTML到系统剪贴板。有没有键绑定它，但你可以通过搜索“降价预览HTML复制”找到它在命令面板。

降价预览在实施[原子/降价预览](https://github.com/atom/markdown-preview)包。

### [](https://atom.io/docs/v0.191.0/using-atom-writing-in-atom#snippets)片段

也有一些伟大的片段可用于快速书写降价。

如果您键入`IMG`和命中`选项卡`，你得到像降价格式的图像嵌入代码`！[]（） `。如果你输入`表`，打`标签`，你得到一个很好的例子表填写。
    
    |头一个|头两个|
    |：------------- |：------------- |
    |项目一|产品二|
    

目前只有极少数人（`B`大胆，`我`为斜体，_代码_的代码块，等等），但它可以很容易地节省您的时间不必查找比较模糊的语法。同样，你可以很容易地看到所有可用的片段的列表文件你目前所打的类型_ALT移-S _。

## 基本自定义

现在，我们都感觉舒服的一切只是内置了凌动，让我们来看看如何调整它。或许是你用了很多，但感觉错了一个键绑定或颜色不适合你完全正确。Atom是极其灵活，让我们去了一些简单的弯曲，它可以做。

### [](https://atom.io/docs/v0.191.0/using-atom-basic-customization#style-tweaks)风格扭动

如果要应用快速和肮脏的个人风格的变化，而 ​​无需创建，你打算公布一个完整的主题，您可以添加样式的`styles.less`在文件`〜/ .atom`目录。

您可以从编辑器中打开该文件_的Atom>打开你的样式_菜单。

![开放式样式表](https://atom-test.s3-us-west-2.amazonaws.com/docs/images/97/9758422b93c836c23abec1b9f31709ab0ee9def4/menubar.png)

打开你的样式表

例如，改变光标的颜色，你可以添加以下规则到你的_〜/ .atom / styles.less_文件：
    
    原子的文本编辑器。是聚焦 .cursor  { 
      边框颜色： 粉色; 
    }
    
    
    atom-text-editor.is-focused .cursor {
      border-color: pink;
    }
    

要查看哪些类可用于样式做的最简单的事情就是通过开发工具手动检查DOM。我们将继续在开发工具非常详细的下一章，但现在让我们来简单了解一下。

您可以通过点击打开开发工具`ALT-CMD-I `，它会弹出Chrome开发工具面板。

![开发工具](https://atom-test.s3-us-west-2.amazonaws.com/docs/images/a8/a8ce24b23e715b74b67016b372bac6f2b84b88f2/devtools.png)

开发工具

现在，您可以轻松地检查你当前编辑器的所有元素。如果您想更新的一些风格，你只需要找出它有什么类，写一个都不能少规则到您的风格文件进行修改。

如果你不熟悉少，这是一个基本的CSS预处理，使一些事情CSS更容易一点。您可以了解更多关于它的[lesscss.org](http://www.lesscss.org/)。如果你喜欢使用CSS来代替，这个文件也可以被命名为_styles.css的_并包含CSS。

### [](https://atom.io/docs/v0.191.0/using-atom-basic-customization#customizing-key-bindings)自定义键绑定

原子键映射的工作方式与样式表。正如样式表使用选择器样式应用到元素，凌动键盘映射使用选择器按键，在特定情况下的事件相关联。这里有一个小例子，从Atom的内置键盘映射摘录：
    
    “原子文本编辑器” ：
      “输入” ： “编辑：换行”
    
    “原子文本编辑器[小]输入” ：
      “进入' ： '核心：确认“
    
    
    'atom-text-editor':
      'enter': 'editor:newline'
    
    'atom-text-editor[mini] input':
      'enter': 'core:confirm'
    

这种键盘映射定义的含义`进入`在两个不同的上下文。在一个正常的编辑，按压`输入`发射`编辑：换行符`事件，这将导致编辑插入一个换行。但是，如果相同的键击发生一个选择列表的迷你编辑器内，它代替发射`芯：确认`基于在更特定的选择的结合事件。

默认情况下，`〜/ .atom / keymap.cson`当凌启动加载。它总是会最后加载，让您有机会来覆盖由凌动核心的键盘布局或第三方软件包定义绑定。

您可以打开从编辑这个文件_的Atom>打开你的键盘对应_菜单。

你想知道的所有可用的命令。打开设置面板（`CMD-， `），然后选择_键绑定_选项卡。它会告诉你所有的键绑定当前正在使用。

### 全局配置设置

凌动载荷从配置设置`config.cson`在文件_〜/ .atom_目录，其中包含CoffeeScript的风格JSON：[CSON](https://github.com/atom/season)。
    
    “核心” ：
      “excludeVcsIgnoredPaths” ： 真正的
    '编辑' ：
      'fontSize的“ ： 18
    
    
    'core':
      'excludeVcsIgnoredPaths': true
    'editor':
      'fontSize': 18
    

配置本身是由分组包名或两个核心命名空间中的一个：`核心`和`编辑器`。

您可以从编辑器中打开该文件_的Atom>打开你的配置_菜单。

#### [](https://atom.io/docs/v0.191.0/using-atom-basic-customization#configuration-key-reference)配置功能参考

  * `核心`

    * `disabledPackages`：包名的数组禁用

    * `excludeVcsIgnoredPaths`：不要通过指定的文件中搜索_的.gitignore_

    * `ignoredNames`：文件名 ​​在所有的Atom忽视

    * `PROJECTHOME`：该目录中的项目被认为是位于

    * `主题`：主题名称的数组装载，在层叠顺序

  * `编辑`

    * `自动缩进`：启用/禁用的基本自动缩进（默认为`真`）

    * `nonWordCharacters`：一串非单词字符定义字边界

    * `fontSize的`：编辑字体大小

    * `fontFamily中`：编辑字体系列

    * `无形`：指定字符的Atom呈现了隐身在这个哈希（使用`虚假的`关闭个性类型）

      * `标签`：硬制表符

      * `CR`：回车（微软风格的行结束符）

      * `EOL`：`\ñ`字符

      * `空间`：开头和结尾的空格字符

    * `preferredLineLength`：标识的线段的长度（默认为`80`）

    * `showInvisibles`：是否呈现占位符不可见字符（默认为`假`）

    * `showIndentGuide`：在编辑器中显示/隐藏缩进指标

    * `showLineNumbers`：排水沟内显示/隐藏行号

    * `softWrap`：启用/在编辑器中禁用文字的软包装

    * `softWrapAtPreferredLineLength`：启用/禁用在软换行`preferredLineLength`

    * `tabLength`：空格选项卡内的数（默认为`2`）

  * `fuzzyFinder`

    * `ignoredNames`：文件忽略**只**在模糊取景器
  * `空白`

    * `ensureSingleTrailingNewline`：是否要减少多换行符到一个在文件的结尾

    * `removeTrailingWhitespace`：启用/禁用空白的分割，线条的末端（默认为`真`）

  * `总结指南`

    * `列`：散列与一个阵列`图案`和`列`密钥以匹配当前的编辑器的列的位置的路径。

### [](https://atom.io/docs/v0.191.0/using-atom-basic-customization#language-specific-configuration-settings)语言特定的配置设置

您还可以设置多个配置设置不同的不同的文件类型。例如，您可能希望凌动软包降价文件，有两个空间选项卡红宝石文件，和四个空间选项卡Python文件。

有几个设置现在作用于编辑的语言。这里是当前列表中：
    
    editor.tabLength
    editor.softWrap
    editor.softWrapAtPreferredLineLength
    editor.preferredLineLength
    editor.scrollPastEnd
    editor.showInvisibles
    editor.showIndentGuide
    editor.nonWordCharacters
    editor.invisibles
    editor.autoIndent
    editor.normalizeIndentOnPaste
    
    
    editor.tabLength
    editor.softWrap
    editor.softWrapAtPreferredLineLength
    editor.preferredLineLength
    editor.scrollPastEnd
    editor.showInvisibles
    editor.showIndentGuide
    editor.nonWordCharacters
    editor.invisibles
    editor.autoIndent
    editor.normalizeIndentOnPaste
    

#### [](https://atom.io/docs/v0.191.0/using-atom-basic-customization#language-specific-settings-in-the-settings-view)在设置查看特定语言的设置

您可以编辑在设置这些配置设置，查看每个语言的基础。只需搜索您所选择的语言在左侧面板中，选择它，并编辑了！

![蟒蛇设置](https://atom-test.s3-us-west-2.amazonaws.com/docs/images/75/7523ae81f744be2f1ff98cc51cd97a729b345e70/python-settings.png)

Python的具体设置

#### [](https://atom.io/docs/v0.191.0/using-atom-basic-customization#language-specific-settings-in-your-config-file)在您的配置文件的特定语言的设置

您也可以直接编辑实际的配置文件。通过命令面板中打开你的配置文件，输入“打开配置”，然后回车。

全局设置下一个全局密钥，并且每个语言都可以有其自己的顶级密钥。这关键是语言的范围。特定语言的设置将覆盖任何在全局部分设置。
    
    “全球性” ： ＃ 所有的 语言 ，除非 重写
      '编辑' ：
        'softWrap“ ： 假
        “tabLength” ： 8
    
    “.source.gfm” ：＃  降价 覆盖
      “编辑” ：
        “softWrap” ： 真实的
    
    “.source.ruby” ：＃  红宝石 覆盖
      “编辑” ：
        “tabLength” ： 2
    
    “.source.python” ：＃  蟒蛇 覆盖
      “编辑” ：
        “tabLength” ： 4
    
    
    'global': # all languages unless overridden
      'editor':
        'softWrap': false
        'tabLength': 8
    
    '.source.gfm': # markdown overrides
      'editor':
        'softWrap': true
    
    '.source.ruby': # ruby overrides
      'editor':
        'tabLength': 2
    
    '.source.python': # python overrides
      'editor':
        'tabLength': 4
    

#### [](https://atom.io/docs/v0.191.0/using-atom-basic-customization#finding-a-language-s-scope-name)找到一个语言的范围名称

为了有效地写这些覆盖，你需要知道的语言范围名称。我们已经做到了这一点查找范围写在一个片段[“片段格式”](https://atom.io/docs/v0.191.0/ch00/_snippet_format)，但是我们可以再次快速覆盖。

的范围名称显示在设置视图每种语言。搜索您所选择的在左侧面板的语言，选择它，你应该看到的语言名称标题下的范围名称：

![蟒蛇语法](https://atom-test.s3-us-west-2.amazonaws.com/docs/images/97/9700446814a5e29d1317e6e1ce656597c589ff0e/python-grammar.png)

查找语言的语法

## 总结

此时，你应该是一个Atom主用户。你应该能够浏览和操作文本和文件就像一个向导。你也应该能够向前和向后定制的Atom，使它看起来和行为，你是多么希望它。

接下来我们将采取下一步行动，这是看变化，增加新的功能，以凌动本身的核心。我们要开始为凌动创建包。如果你有梦想，你可以建造它。

# Hacking Atom

现在是时候来的容易被破解编辑器的“被破解”的一部分。正如我们已经看到整个第二节，凌动的很大一部分是由捆绑包。如果你想添加一些功能的Atom，您可以访问相同的API和工具，凌动的核心功能了。从[树视图](https://github.com/atom/tree-view)的[命令面板](https://github.com/atom/command-palette)，以[查找和替换](https://github.com/atom/find-and-replace)功能，凌动的，即使是最核心的功能是实现为包。

## 贸易工具

首先，有几件事情，我们将假定你知道，至少在一定程度上。由于所有的Atom使用Web技术实现，我们必须假设你知道的Web技术，如JavaScript和CSS。具体而言，我们将实现一切的CoffeeScript少，这是预处理器分别Javascript和CSS。

如果你不知道的CoffeeScript，但你熟悉JavaScript，你不应该有太多的麻烦。下面是一些简单的CoffeeScript代码的示例：
    
    MyPackageView = 需要 './my-package-view“
    
    module.exports = 
      myPackageView：空
    
      激活：（州） - > 
        @myPackageView = 新 MyPackageView （状态。myPackageViewState ）
    
      取消：- > 
        @myPackageView 。破坏（）
    
      连载：- > 
        myPackageViewState：@myPackageView 。序列化（）
    

我们就去了这样的例子一点，但是这是什么语言的样子。

只是一切你可以在CoffeeScript的凌动做也是可行的在JavaScript中，但由于大多数社区使用的CoffeeScript，你可能会想在里面写你的包。这将帮助你得到的捐款来自社会，在许多情况下，写简单的代码。

您可以在CoffeeScript的刷在[coffeescript.org](http://coffeescript.org/)。

少即是从CSS更简单的过渡。它增加了许多功能，如变量和函数CSS有用的东西。您可以在更少的技能刷上去的[lesscss.org](http://lesscss.org/)。我们少的使用不会得到在这本书中却过于复杂，所以只要你知道基本的CSS你应该罚款。
