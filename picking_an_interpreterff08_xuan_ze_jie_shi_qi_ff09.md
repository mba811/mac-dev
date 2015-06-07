# Picking an Interpreter（选择解释器）

## The State of Python (2 vs 3)（Python的形势）

> When choosing a Python interpreter, one looming question is always present: “Should I choose Python 2 or Python 3”? The answer is not as obvious as one might think.

当选择一个Python解释器的时候，总是存在一个迫在眉睫的问题：“我应该选择Python 2还是Python 3？”答案并不像我们想象的那么简单。

> The basic gist of the state of things is as follows:
> 
>   1. Python 2.7 has been the standard for a long time.
>   2. Python 3 introduced major changes to the language, which many developers are unhappy with.
>   3. Python 2.7 will receive necessary security updates for a few years.
>   4. Python 3 is continually evolving, like Python 2 did in years past.
> 
> So, you can now see why this is not such an easy decision.

事态的一些基本讨论点如下：

  1. Python 2.7成为标准已经很长时间。
  2. Python 3引进了一些许多开发者都不太满意的巨大变化。
  3. Python 2.7将得到已经更新多年的安全性。
  4. Python 3正像多年前的Python 2持续发展。

所以，你现在可以发现做决定并没有那么容易。

## Recommendations（建议）

> I’ll be blunt:

我会迟疑：

> **Use Python 3 if...**
> 
>   * You don’t care.
>   * You love Python 3.
>   * You are indifferent towards 2 vs 3.
>   * You don’t know which one to use.
>   * You embrace change.

如果使用Python 3...

  * 你不在乎。
  * 你喜欢Python 3。
  * 你不关心2 vs 3。
  * 你不知道要用哪个。
  * 你热衷于变化。

> **Use Python 2 if...**
> 
>   * You love Python 2 and are saddened by the future being Python 3.
>   * The stability requirements of your software would be improved by a language and runtime that never changes.
>   * Software that you depend on requires it.

如果使用Python 2...

  * 你喜欢Python 2并且不看好Python 3的未来。
  * 你的软件稳定性需求可以通过语言和运行状态不变来改善。
  * 你所依赖的软件需要Python 2。

## So.... 3?

> If you’re choosing a Python interpreter to use, and aren’t opinionated, then I recommend you use the newest Python 3.x, since every version brings new and improved standard library modules, security and bug fixes. Progress is progress.

如果你正在选择使用一种Python解释器，而且不那么固执己见的话，我会推荐你使用最新版的Python 3.x，因为每个版本都会带来新的和改进后的标准库模块、安全性和bug修复。前进就是进步。

> Given such, only use Python 2 if you have a strong reason to, such as a Python 2 exclusive library which has no adequate Python 3 ready alternative, or you (like me) absolutely love and are inspired by Python 2.

鉴于以上，如果你有特别原因的话你应该只用Python 2，比如一些Python 2特有库在Python3中还没有合适的替代品，或者是你（就像我一样）对Python 2有着绝对的爱和灵感。

> Check out [Can I Use Python 3?](https://caniusepython3.com/) to see if any software you’re depending on will block your adoption of Python 3.

检查一下[Can I Use Python 3?](https://caniusepython3.com/)这篇文章看看有没有阻止你采用Python 3的依赖软件。

[Further Reading](http://wiki.python.org/moin/Python2orPython3)

> It is possible to write code that works on Python 2.6, 2.7, and 3.3. This ranges from trivial to hard depending upon the kind of software you are writing; if you’re a beginner there are far more important things to worry about.

很可能在Python 2.6, 2.7和3.3上你都可以写代码，你正在编写的软件决定了这将是微不足道的还是特别困难的；当然如果是一个初学者的话你要担心的事情远比这重要。

## Implementations（安装使用）

> When people speak of Python they often mean not just the language but also the CPython implementation. Python is actually a specification for a language that can be implemented in many different ways.

当人们谈论Python的时候并不总指的这门语言，而且还是CPython的实现。Python其实是这门语言的一种规范，可以通过不同的方式实现。

### CPython

> CPython is the reference implementation of Python, written in C. It compiles Python code to intermediate bytecode which is then interpreted by a virtual machine. CPython provides the highest level of compatibility with Python packages and C extension modules.

CPython是Python的参考实现，采用C语言编程。它可以将Python代码编译成可以被虚拟机解释的中间字节码。CPython可以为Python包和C扩展模块提供最好的兼容性。

> If you are writing open-source Python code and want to reach the widest possible audience, targeting CPython is best. To use packages which rely on C extensions to function, CPython is your only implementation option.

如果你正在编写Python开源代码并且希望达到尽可能广泛的关注，那最好针对CPython。为了使用依赖于C扩展功能的包，CPython将是你的唯一选择。

> All versions of the Python language are implemented in C because CPython is the reference implementation.

所有的Python版本都是在C中实现的，因为CPython是标准参考实现。

### PyPy

> PyPy is a Python interpreter implemented in a restricted statically-typed subset of the Python language called RPython. The interpreter features a just-in-time compiler and supports multiple back-ends (C, CLI, JVM).

PyPy是一种限制于静态类型化的Python语言子集（称为RPython）的一种Python解释器实现。这种解释器包含JIT即时编译特性，并且支持多种后端（C, CLI, JVM）。

> PyPy aims for maximum compatibility with the reference CPython implementation while improving performance.

PyPy的目标在于CPython参考实现的最大兼容性，同时改善性能。

> If you are looking to increase performance of your Python code, it’s worth giving PyPy a try. On a suite of benchmarks, it’s currently over 5 times faster than CPython.

如果你想提高Python代码的性能，那么PyPy值得一试。在某套标准之下，目前PyPy比CPython快了5倍。

> PyPy supports Python 2.7. PyPy3 [[1](http://jimmylv.gitbooks.io/python-guide-zh/content/GLOSSARY.html#1)], released in beta, targets Python 3.

PyPy支持Python 2.7。PyPy3已经发布beta版，目标指向Python 3。

### Jython

> Jython is a Python implementation that compiles Python code to Java bytecode which is then executed by the JVM (Java Virtual Machine). Additionally, it is able to import and use any Java class like a Python module.

Jython是另一种Python实现，它可以将Python代码编译成可以被JVM（Java虚拟机）执行的Java字节码。此外，它也可以像Python模块一样导入和使用任何Java类。

> If you need to interface with an existing Java codebase or have other reasons to need to write Python code for the JVM, Jython is the best choice.

如果你需要接口连接已存在的Java代码库或者有其他需要为JVM编写Python代码的原因，Jython是最好选择。

> Jython currently supports up to Python 2.5. [2]

Jython最近已经支持Python 2.5。

### IronPython

> IronPython is an implementation of Python for the .NET framework. It can use both Python and .NET framework libraries, and can also expose Python code to other languages in the .NET framework.

IronPython是Python在.NET平台的一种实现。它可以同时使用Python和.NET框架的所有库，也可以给在.NET平台下的其他语言使用Python代码。

> Python Tools for Visual Studio integrates IronPython directly into the Visual Studio development environment, making it an ideal choice for Windows developers.

Python在VS上的工具可以直接将IronPython直接集成到VS开发环境中，使其成为Windows开发者的理想选择。

> IronPython supports Python 2.7. [3]

IronPython支持Python 2.7。

## PythonNet

> Python for .NET is a package which provides near seamless integration of a natively installed Python installation with the .NET Common Language Runtime (CLR). This is the inverse approach to that taken by IronPython (see above), to which it is more complementary than competing with.

Python for .NET是一个提供无缝继承.NET CLR的Python本地安装包。这是跟上面的IronPython采用相反的方法，将会形成互补而不是竞争。

> In conjunction with Mono, PythonNet enables native Python installations on non-Windows operating systems, such as OS X and Linux, to operate within the .NET framework. It can be run in addition to IronPython without conflict.

通过结合Mono，PythonNet可以使本机的Python安装在其他像OS X和Linux这样的非Windows系统，运行时无需.NET平台。它可以完全无冲突运行，除了IronPython。

> PythonNet supports from Python 2.3 up to Python 2.7. [4]

PythonNet支持Python 2.3到Python 2.7。

[[1](http://jimmylv.gitbooks.io/python-guide-zh/content/GLOSSARY.html#1)] [http://pypy.org/compat.html](http://pypy.org/compat.html) [2][http://wiki.python.org/jython/JythonFaq/GeneralInfo#Is_Jython_the_same_language_as_Python.3F](http://wiki.python.org/jython/JythonFaq/GeneralInfo#Is_Jython_the_same_language_as_Python.3F) [3][http://ironpython.codeplex.com/releases/view/81726](http://ironpython.codeplex.com/releases/view/81726) [4] [http://pythonnet.github.io/readme.html](http://pythonnet.github.io/readme.html)
