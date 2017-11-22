# Python 科学计算
本课主要介绍科学计算，实验环境的安装以及使用等内容。

本实验环境采用带桌面的Ubuntu Linux环境，代码编写与命令运行都会在 Spyder IDE 上进行。Spyder 是一个类 MATLAB IDE 专注于科学计算的 Python IDE。

## 实验目录
1. 计算在科学中所扮演的角色
2. 科学计算的要求
> > -  管理源代码的工具
3. 为什么Python适合科学计算?
> > - 科学 Python 软件栈
4. Python 环境
> > - IPython
> > - IPython notebook
> > - Spyder
> > - Python的版本
5. 安装
> > - Linux
> > - Windows

##  1 计算在科学中所扮演的角色
传统意义上科学被分为两类：经验科学与理论科学，但在过去的几十年中计算渐渐成为了科学重要的一部分。科学计算在接近理论的同时又包含很多实验工作的特性，因此常常被看作是科学的第三分支。在大多数领域中，计算工作是对经验与理论的一个重要补充，现今大量的论文都包含了数值计算，计算机模拟和建模。

在经验科学与理论科学的领域中已经建立起了完善的规则使得研究结果可以被获取。而在计算机科学中却没有好的指导规范规定源代码与数据必须发布，最近这个议题越来越受到人们的关注，一些著名的期刊，包括科学，都在呼吁论文作者提供处理数据的源代码，这场关于如何促进源代码分发的讨论将持续进行。

## 2 科学计算的要求
可复制 与 可重现 是科学方法的两块基石。对于数值工作，遵守这些概念有以下两点实际意义：

> > - 可复制：有需要时论文作者能够重新模拟一次并且复制结果，其他科学家在进行相同的计算后应当能得到同样的结果。

> > - 可重现：数值模拟所得到的结果可以由方法的独立实现来重现，或者是完全不同的方法来重现。

结论：一个可靠的科学结果应当是可重现的， 一个可靠的科学研究应当是可复制的。

为了实现这些目标，我们需要：

> - 准确地记录下产生论文数据与图表的源代码及其版本号。

> - 记录下所使用的软件的版本号等信息，确保实验环境是能够还原的。

> - 确保旧代码与笔记已经备份，为以后可能的引用做准备

> - 在理想情况下将源代码发布到线上，使其它对其感兴趣的科学家能很容易得到它。

### 2.1 管理源代码的工具
保证科学模拟的可复制与可重现是一个麻烦的工作，不过有很多好的工具能帮到你：

> - 版本控制系统 (RCS) 软件：

> > - git - http://git-scm.com
> > - mercurial - http://mercurial.selenic.com 也就是 hg
> > - subversion - http://subversion.apache.org 也就是 svn
> - 线上源代码仓库：

> > - Github - http://www.github.com
> > - Bitbucket - http://www.bitbucket.com

## 3 为什么Python适合科学计算?
- Python 在科学计算中有着重要地位:
> > - 大量的社区用户, 易于寻求帮助与查询文档。
- 在科学计算库方面有着近乎完美的生态系统：
> > - numpy: http://numpy.scipy.org - Numerical Python
> > - scipy: http://www.scipy.org - Scientific Python
> > - matplotlib: http://www.matplotlib.org - graphics library
- 极佳的性能 —— 集成了用 C 与 Fortran 写的经过高度优化的代码:
> > - blas, altas blas, lapack, arpack, Intel MKL, ...
- 良好的支持
> > - 多进程多线程平行计算
> > - 进程间通信 (MPI)
> > - GPU 计算 (OpenCL 与 CUDA)
- 容易获取，适合高性能计算机集群。
- 不需要许可证费用。


## 4 Python 环境

这里介绍几种科学计算会使用到的 python 环境

### 4.1 IPython

IPython是一种基于Python的交互式解释器。相较于原生的Python Shell，IPython提供了更为强大的编辑和交互功能。

![image](https://dn-anything-about-doc.qbox.me/document-uid8834labid1075timestamp1468326131599.png/wm)

IPython 的特性包括:

> - 命令历史记录
> - Tab 自动补全
> - 对象自省，自动提取对象的文档内容
> - 与操作系统 shell 有良好的交互
> - 支持后端多平行线程，可以运行在计算集群或者云服务上

### 4.2 IPython notebook
IPython notebook是一个基于HTML的 notebook 环境, 类似于 Mathematica 或者 Maple。

![image](https://dn-anything-about-doc.qbox.me/document-uid8834labid1075timestamp1468326230395.png/wm)

尽管使用web浏览器作为图形接口，IPython notebooks 一般都在本地运行，要开启一个新的

IPython notebook，可以运行以下命令：


```
$ ipython notebook <directory>
```

### 4.3 Spyder
Spyder 是一个类 MATLAB IDE 的 Python IDE。 它拥有传统IDE环境所拥有的的优点。

![image](https://dn-anything-about-doc.qbox.me/document-uid8834labid1075timestamp1468326284723.png/wm)

Spyder 的优点:

> - 强大的代码编辑器，动态代码自省，内集成 python 调试器。
> - 变量浏览器，IPython 命令行终端。
> - 集成了文档与帮助。

### 4.4 Python的版本
Python 有两个版本：Python2 与 Python3。Python3 最终会取代 Python2， 但它并没有兼容 Python2， 大量现存的 python 代码与包是用 Python2 写的，它也仍然是最广泛使用的版本。不过在本实验中，Python2 或是Python3都是可以的。

输入以下命令查看 Python 版本：

```
$ python --version
Python 2.7.3
$ python3.2 --version
Python 3.2.3
```

## 5 安装
### Linux

在 Ubuntu Linux 中安装科学计算所用的工具:

```
$ sudo apt-get install python ipython ipython-notebook
$ sudo apt-get install python-numpy python-scipy python-matplotlib python-sympy
$ sudo apt-get install spyder
```

### Windows

Windows 缺乏一个好的包管理系统，所以搭建一个 Python 环境最简单的方法就是安装一个科学计算发行版：

> - Enthought Python Distribution. EPD 是商业产品，不过如果是为了学术目的则可以免费获取。
> - Anaconda CE. Anaconda Pro 是商业产品， 不过 Anaconda 社区版是免费的。
> - Python(x,y). 开源。



