---
layout: post
title:笨办法学Python
date: 2020-2-21
categories: blog
tags: [学习，黑客]
description: 记录黑客成长路！
---

**记录 Python 学习路**

### 20200229

2020-2-29 17:02:46

- 官方文档，讲解很详细

  [Python 教程 — Python 3.7.6 文档](https://docs.python.org/zh-cn/3.7/tutorial/index.html)

- Python 安装教程

   [Python 环境安装教程（Windows）](https://blog.csdn.net/qq_36667170/article/details/79275605)

2020-2-29 16:45:22

如果安装好了，但是python还是不能被识别，那你需要在PowerShell下输入并执行以下命令：

```[Environment]::SetEnvironmentVariable("Path", "$env:Path;C:\Python27", "User")```

必要是重启 PowerShell，重启电脑。

**Python 多版本安装**

终极解决方案

[电脑同时安装了python2和python3后，随意切换版本并使用pip安装 - 南山散人 - 博客园](https://www.cnblogs.com/python-kp/p/9361926.html)

ref:

* [通过cmd切换python2和python3版本_Python_YoungfreeFJS的博客-CSDN博客](https://blog.csdn.net/qq471011042/article/details/81067107)
* [使用Anaconda实现Python2和Python3共存及相互转换 - 简书](https://www.jianshu.com/p/fe327b72fa31)

上面两种方法均需要安装 Anaconda ，且 activate 命令在powershell 中需要版本 在4.4 以上

**方法归纳** 

1. 跳出问题看问题
2. 不要死扣一个问题

2020-2-29 14:57:41

如果需要使用 Pycharm 又恰好是学生的话，可以免费申请享用高大上的Professional版本。

- 申请地址：https://www.jetbrains.com/student/

在填写学校邮箱申请完成后，会收到一封激活邮件。点击链接激活后会收到一封包含下载地址链接的邮件，就可以享用 Jetbrains 的所有专业软件了。

2020-2-29 14:48:32

[[K萌君]教你做Windows + Ubuntu双系统](https://www.bilibili.com/video/av9855447)

2020-2-29 14:38:33

**windows文件和Linux文件的位置**
要是想在Ubuntu里查看windows分区里面的文件可以在/mnt埋面查看要是想在windows里面查看Ubuntu里面的文件，在我电脑上的位置是
C:\Users\你的用户名\AppData\Local\Packages\CanonicalGroupLimited.UbuntuonWindows_ 79rhkp1fndgsc\LocalState/rootfs



**因为没有内核导致的-些坑**
没有真正的Linux Kernel,所以mtr, traceroute, iptables都用不了， docker 用不了。装apache会捆绑ufw,结果ufw也用不了。因此重度依
赖内核的东西还是算了，不能在上面搞。



2020-2-29 13:18:18 

在 Windows 上安装 Ubuntu 子系统[^2.29.13]

[^2.29.13]:[不用装双系统，直接在 Windows 上体Linux：Windows Subsystem for Linux - 少数派](https://sspai.com/post/43813) 

[用 Linux 为主力系统，也能有 Windows 一样的使用体验 - 少数派](https://sspai.com/post/38895)

虚拟机

- [VMware 中国 – 云计算、移动化与网络和安全解决方案 | CN](https://www.vmware.com/cn.html)
- [virtualbox](https://www.virtualbox.org/)

### 20200228

2020-2-28 22:09:10

[python 在powershell中运行中文乱码时有时无怎么办？ - SegmentFault 思否](https://segmentfault.com/q/1010000004406660) 

2020-2-28 14:24:01

python 中 exit(0) 和 exit()1 有什么功能？
在很多类型的操作系统里，exit(0) 可以中断某个程序，而其中的数字参数则用来表示程序是否是碰到错误而中断。exit(1) 表示发生了错误进行退出，而 exit(0) 则表示程序是正常退出的，退出代码是告诉解释器的（或操作系统）。这和我们学的布尔逻辑 0==False 正好相反，不过你可以用不一样的数字表示不同的错误结果。比如你可以用 exit(100) 来表示另一种和 exit(2) 或 exit(1) 不同的错误。

2020-2-28 12:40:48

[笨方法学python3: ex43中文魔改_CSDN博客](https://blog.csdn.net/weixin_39518371/article/details/82958054) 

### 2020-2-27

2020-2-27 14:39:23

撰文一篇，**将 Markdown 转换成网页版 PPT**

- 不能直接转换成 PPT
- 可以具有 PPT 的效果
- 使用[reveal-md](https://github.com/webpro/reveal-md)，高阶使用 reveal.js
- 介绍命令行的使用

2020-2-27 13:48:50

- 设置主题为白色

```powershell
PS F:\explore> reveal-md .\20200227demo.md --theme white
```



- 支持多个命令同时执行，设置主题为白色，并打印为 pdf

```powershell
PS F:\explore> reveal-md .\20200227demo.md --theme white --print
```



PS F:\explore> reveal-md .\20200227demo.md --theme white

2020-2-27 13:30:36

记录问题的过程就伴随着问题的解决



问题描述

在 PowerShell 中运行命令后，不能自动退出，也不能移动光标，只能重新关掉 PowerShell 重新进行操作，太过麻烦。

```powershell
PS F:\explore> reveal-md .\20200227demo.md print
Reveal-server started at http://localhost:1948


```

百度搜索： 如何使用 PowerShell 关闭程序命令

都是一堆用 PowerShell 关闭程序运行的。

还有说 `exit` 命令，也无济于事。

想想可能是提问方式不对，这应该是有自己不会的操作。

比如进入 Python 对话编译器是 `Ctrl + Z` ,于是搜索 “ PowerShell快捷键“，查找到：

> Ctrl+C	取消正在执行的命令

进行执行

```powershell
PS F:\explore> reveal-md .\20200227demo.md print
Reveal-server started at http://localhost:1948
Received SIGINT, closing gracefully.
```

成功！

总结两点：

1. 换个提问方式
2. 多看几个回答，至少三个
3. 瞄准问题答案

2020-2-27 12:59:56

[命令行补充](https://www.baidu.com/link?url=eHljczvC0OU4XDlG4CKUnBpF2mgKDpUjc6_OcfO8B_v1JNNuz9U2Eau9LlbdMTOa&wd=&eqid=d9369dcb0027c042000000035e574c35)

2020-2-27 12:35:39

Docker 是一个开源的应用容器引擎，基于 [Go 语言](https://www.runoob.com/go/go-tutorial.html) 并遵从 Apache2.0 协议开源。

Docker 可以让开发者打包他们的应用以及依赖包到一个轻量级、可移植的容器中，然后发布到任何流行的 Linux 机器上，也可以实现虚拟化。

容器是完全使用沙箱机制，相互之间不会有任何接口（类似 iPhone 的 app）,更重要的是容器性能开销极低。

Docker 从 17.03 版本之后分为 CE（Community Edition: 社区版） 和 EE（Enterprise Edition: 企业版），我们用社区版就可以了。

[Docker教程 ](https://www.runoob.com/docker/docker-tutorial.html)

2020-2-27 12:28:26

YAML 是 "YAML Ain't a Markup Language"（YAML 不是一种标记语言）的递归缩写。在开发的这种语言时，YAML 的意思其实是："Yet Another Markup Language"（仍是一种标记语言）。

YAML 的语法和其他高级语言类似，并且可以简单表达清单、散列表，标量等数据形态。它使用空白符号缩进和大量依赖外观的特色，特别适合用来表达或编辑数据结构、各种配置文件、倾印调试内容、文件大纲（例如：许多电子邮件标题格式和YAML非常接近）。

YAML 的配置文件后缀为 **.yml**，如：**runoob.yml** 。



编程免不了要写配置文件，怎么写配置也是一门学问。

YAML 是专门用来写配置文件的语言，非常简洁和强大，远比 JSON 格式方便。

本文介绍 YAML 的语法，以 [JS-YAML](https://github.com/nodeca/js-yaml) 的实现为例。你可以去[在线 Demo](http://nodeca.github.io/js-yaml/) 验证下面的例子。[^1]

[^1]:[YAML语法 ——阮一峰](http://www.ruanyifeng.com/blog/2016/07/yaml.html)

2020-2-27 12:08:49

[Reveal-md ](https://www.jianshu.com/p/24cb76c07754) 

[Reveal-md Github介绍](https://github.com/webpro/reveal-md)

2020-2-27 11:43:22

[Markdown+pandoc+reveal.js 做网页 PPT - 简书](https://www.jianshu.com/p/9b71614f57b1)

2020-2-27 10:39:39

- ### 一些快捷键

  - ← ↑ → ↓: 控制幻灯片的切换。
  - ESC：对幻灯片做个整体的概览。
  - ALT+click ：类似 PowerPoint 放映的时候的放大镜的效果，镜头迅速拉近。
  - S：开启演讲者模式，这点和 PowerPoint 类似，分成四个板块：当前幻灯片的显示，下一张幻灯片的预览，当前演讲时间以及演讲的备注笔记。
  - B：暂时停止当前的幻灯片的放映，呈现黑屏。在演讲时，当你希望听众能把注意力集中在你身上的时候，非常有用。

  [用 reveal.js 随心所欲地制作 PPT](https://sspai.com/post/42179)

幻灯片的内容需要包含在<div> <div>的标签中。

一个 section 是一页幻灯片。

如果你将多个 <section> 放到另一个 < section> 的内部，它们将会以垂直幻灯片的方式显示。第一个垂直幻灯片是其它的 “root（根）”

怎么理解呢？ 可以这样理解：横向的幻灯片代表一章，纵向的幻灯片代表一章中的一节。那么横向的幻灯片在播放时是左右切换的，而纵向的幻灯片是上下切换的。

ppt的储存

参见

[网页PPT： reveal.js 介绍——腾讯云](https://cloud.tencent.com/developer/article/1195003)

http://yisibl.github.io/share/the-beauty-of-center-in-CSS.html#/

[原网站链接翻译](https://www.awesomes.cn/repo/hakimel/reveal-js)

[官网](https://github.com/hakimel/reveal.js)

[Reveal.js：把你的 Markdown 文稿变成 PPT——少数派](https://sspai.com/post/40657)

```powershell
pandoc slides.md -o slides.html -t revealjs -s -V theme=white
```



[使用 Reveal.js 做交互式在线PPT的心得——知乎](https://zhuanlan.zhihu.com/p/83425852)

### 2020-2-26

今日没有完成任务，

1. **输入大段代码，不再恐惧** 。更喜欢用命令行解决问题。阅读代码的能力还需要增强。

2. 成功解决 `cnpm` 不能使用的问题。

3. 体会到 GitHub 工具的伟大性，关键步骤又提交，凝练改动结果，进行提交

4. 发现优质图床管理软件，[PicGo](https://picgo.github.io/PicGo-Doc/zh/guide/#下载安装)支持，Windo、Mac 和Linux

   typro支持 Picgo插件

   ![mark](http://rsc.waterfree.club/rsc/20200226/71jkfOWUL8z7.png)

   另外发现本页面是使用 gitbook 托管生成

**2020-2-26 22:09:55**

概念是参照于一个来自《[程序员修炼之道](https://baike.baidu.com/item/程序员修炼之道/7872985)》书中的一个故事。传说中程序大师随身携带一只小黄鸭，在调试代码的时候会在桌上放上这只小黄鸭，然后详细地向鸭子解释每行代码 [1] 。
　　许多程序员都有过向别人（甚至可能向完全不会编程的人）提问及解释编程问题，就在解释的过程中击中了问题的解决方案。一边阐述代码的意图一边观察它实际上的意图并做调试，这两者之间的任何不协调会变得很明显，并且更容易发现自己的错误。如果没有玩具小鸭子也可以考虑向其它东西倾诉，比如桌上的花花草草，键盘鼠标。

![](https://bkimg.cdn.bcebos.com/pic/63d0f703918fa0ecb89a22ea2a9759ee3c6ddbfc?x-bce-process=image/resize,m_lfit,w_268,limit_1/format,f_jpg)

**2020-2-26 21:40:11**

命令行的语法解释

```powershell
$ picgo -h

  Usage: picgo [options] [command]

  Options:

    -v, --version                 output the version number
    -d, --debug                   debug mode
    -s, --silent                  silent mode
    -c, --config <path>           set config path
    -h, --help                    output usage information

  Commands:

    install|add <plugins...>             install picgo plugin
    uninstall|rm <plugins...>            uninstall picgo plugin
    update <plugins...>                  update picgo plugin
    set|config <module> [name]           configure config of picgo modules
    upload|u [input...]                  upload, go go go
    use [module]                         use modules of picgo
    init [options] <template> [project]  create picgo plugin's development templates
```

>**提示**
>
>其中，命令选项如果是用`<>`包围起来的为必须输入项，如果是用`[]`包围起来的则为可选输入项。 有些命令支持简写，比如`picgo upload`可以写为`picgo u`。

ref: [PicGo-Core--CLI命令](https://picgo.github.io/PicGo-Core-Doc/zh/guide/commands.html#use)

2020-2-26 21:33:17

**node.js  yarn npm **

参见[node.js、yarn、npm到底是什么？](https://www.cnblogs.com/wendyw/p/11494036.html)

**Node.js**： JavaScript 是 Web 的编程语言，node.js 就是运行在服务端的 JavaScript。

Npm：node.js 一起安装的包管理工具。

比如：我们要使用模块 A，而模块 A 又依赖模块 B，模块 B 又依赖于模块 X 和 Y，npm 可以根据依赖关系，把所有依赖的包都下载下来并管理起来。单纯通过访问页面一个个脚本进行下载是没有办法进行的。

npm 由 3 个独立的部分组成：网站、注册表 (registry)、命令行工具（CLI）

CLI 通过命令行或终端运行，开发者通过 CLI 与 npm 打交道。**命令行的重要性** 。

所以，必须会命令行。

2020-2-26 20:13:39

**目录**

上计算机课时，老师会给自己将目录，讲什么相对路径，绝对路径，感觉没有什么卵用。后来看到有人说 Mac 支持树形目录，Win 不支持，云里雾里的。

后来才知道 目录 ，路径 是多么重要的概念， 应用阳志平先生的划分，一切事物都可以拆分成 **空间**、**时间** 和 **变量**。路径就是告诉找到这个文件的位置，找到位置才能执行命令。

百度百科解释：

> 根目录指逻辑驱动器的最上[一级目录](https://baike.baidu.com/item/一级目录/8932671)，它是相对[子目录](https://baike.baidu.com/item/子目录/4728026)来说的。打开“我的电脑”，双击C盘就进入C盘的根目录，双击D盘就进入D盘的根目录。其它类推。
>
> 根目录在文件系统建立时即已被创建，其目的就是存储子目录（也称为文件夹）或文件的目录项。一“棵“目录树，树的最根本就是它的根（根目录）。

还是太过抽象，我们拿解压到磁盘根目录为例，

[**什么叫解压到磁盘根目录下?怎么样理“根目录”**](http://ask.zol.com.cn/x/4662958.html)

简单,根目录就是在某个盘的直接管理,没有在其他的文件夹下面,比如D盘,就只能在D盘下,D盘有两个文件夹"我的学习资料" ,"我的音乐"都不能在这两个文件夹中,这属于子文件夹了

**一点启示**： 抽象的问题不妨结合一个具体的例子就很清楚了。

[目录表示方式~/与..\分别什么意思，有什么区别？](https://zhidao.baidu.com/question/551960216836350652.html)

> <directory>起限制对目录A的访问的作用，即只允许指定的用户访问A这个目录，通常是指需要登录。
> ~ \代表主目录，假设你登陆的用户名为user，~ /就表示 /home/user；
> ..\是指上级目录，如果这个[xml文件](https://www.baidu.com/s?wd=xml文件&tn=SE_PcZhidaonwhc_ngpagmjz&rsv_dl=gh_pc_zhidao)在目录C中，那么C就是包含在文件夹B中的；
> ..\..\是指上级目录的上级目录。

文件位置

`PS C:\Users\lenovo\desktop\others\clock.py`



相对路径

```powershell
PS C:\Users\lenovo\desktop> python .\others\clock.py
```

绝对路径

```powershell
PS C:\Users\lenovo\desktop> python C:\Users\lenovo\desktop\others\clock.py 
```

在文件目录执行命令

```powershell
PS C:\Users\lenovo\desktop\others> python clock.py
```

文件不过来，命令走过去。命令过来，适合文件比较多分布在同一个文件

对比上述三种方式

```powershell
PS C:\Users\lenovo\desktop> python .\others\clock.py # 相对路径
PS C:\Users\lenovo\desktop\others> python clock.py #在文件目录执行命令
PS C:\Users\lenovo\desktop> python C:\Users\lenovo\desktop\others\clock.py #绝对路径
```

==调整顺序==

走过来，走过去比较麻烦，不如让 命令 统摄全局

全局环境变量

属性

命令行

==增加具体细节== 



另外在 命令行应用中一般 `.`  是当前命令，`..` 是上级目录，`cd ..` 帮助我们返回上层目录。

**cnpm** 包安装不能使用问题

npm 是包安装管理工具，能够通过在终端输入 命令行进行下载，但是 npm 服务器在国外，下载不稳定，于是使用淘宝镜像源进行下载，但是在 win 10 安装后，运行 `cnpm` 命令，提示

```powershell
cnpm : 无法加载文件 C:\Users\hp\AppData\Roaming\npm\cnpm.ps1，因为在此系统上禁止运行脚本。有关详细信息，请参阅 https:/go.microsoft.com/fwlink/?LinkID=135170 中的  
about_Execution_Policies。
所在位置 行:1 字符: 1
 cnpm install amfe-flexible
+ ~~~~
    + CategoryInfo          : SecurityError: (:) []，PSSecurityException
    + FullyQualifiedErrorId : UnauthorizedAccess
————————————————

```

解决方法:

1. 以**管理员身份**运行power shell (cmd 不行)
2. 输入 `set-ExecutionPolicy RemoteSigned` 显示
3. "C:\Users\lenovo\Desktop\公众号二维码0.5m.jpg"

```powershell
PS C:\WINDOWS\system32> set-ExecutionPolicy RemoteSigned

执行策略更改
执行策略可帮助你防止执行不信任的脚本。更改执行策略可能会产生安全风险，如
 https:/go.microsoft.com/fwlink/?LinkID=135170 中的
about_Execution_Policies 帮助主题所述。是否要更改执行策略?
[Y] 是(Y)  [A] 全是(A)  [N] 否(N)  [L] 全否(L)  [S] 暂停(S)  [?] 帮助
(默认值为“N”):
```

3.  然后输入A 回车 问题解决

更多内容 [npm 与 cnpm](https://www.jianshu.com/p/115594f64b41)

摘录：

`-g`：全局安装。 将会安装在C：\ Users \ Administrator \ AppData \ Roaming \ npm，**并且写入系统环境变量**；非全局安装：将会安装在当前定位目录;全局安装可以通过命令行任何地方调用它，本地安装将安装在定位目录的node_modules文件夹下，通过要求调用; 



ex41习题辅助jieda

[]()

[ex41](https://blog.csdn.net/xjc0518/article/details/100623266)

<img src="http://rsc.waterfree.club/rsc/20200226/Ld5vXG9BgldF.png" alt="mark" style="zoom:33%;" />

### 2020-2-25 

今日复盘

**任务**

1. ex46 项目骨架【完成】
2. class 与 object 的区别与联系。 object 是特殊的类，解决 Python class 设计缺陷
3. Explore 微信小程序申请流程 图灵机器人使用

**反思**

- search 不能代替思考，不能解决问题。
- 在搜寻问题解决途径时，应该控制注意力
- 学会查看说明文档

2020-2-25 18:05:43

Python 使用 `pip` ，命令下载软件安装包，  `pip` 基本用法是

Usage： pip COMMAND [OPTIONS]

在 Python 中使用 help → help> pip 可以查看 pip 安装目录

详情见 https://pip.pypa.io/en/stable/

### 2020-2-24

2020-2-24 18:13:52

**Python 中 pass 的作用** 

pass 一般用于占位置。

在 Python 中有时候会看到一个 def 函数:

```python
def sample(n_samples):
    pass
```

该处的 pass 便是占据一个位置，因为如果定义一个空函数程序会报错，当你没有想好函数的内容是可以用 pass 填充，使程序可以正常运行。

2020-2-24 17:36:35

`.pyw`  格式是被设计用来运行开发的纯图形界面程序的，纯图形界面的用户不需要看到控制台

`.pyc` 是 Python 解释器运行程序的中间文件

2020-2-24 15:36:35

书要交叉看，没有一本书可以告诉你全部故事。

《笨办法学Python》循序渐进，语言亲切，题目难度循序渐进，在自己敲代码的过程中理解代码相关概念。

《Python编程快速上手——让繁琐工作自动化》注重交互式方式运行 Python， 有很多实例。

[Python3教程——廖雪峰](https://www.liaoxuefeng.com/wiki/1016959663602400) ，免费中文，讲解也是很简洁凝练，尤其是对 TCP/IP 通信协议，一篇文章就让自己知道怎么回事了。

《利用Python进行数据编程》稍难，和数据相关，算是自己的专项训练。

2020-2-24 15:36:35

面向对象与面向过程的区别，一个是蛋炒粉，一个是盖浇饭，前者不容易拆分，后者容易独立操作==待修订== 

详见知乎[(2分钟让你明白什么是面向对象编程)](https://zhuanlan.zhihu.com/p/75265007)

类的定义是为面向对象提供技术支撑。

**搜索中文答案**：学习 Python 初始，我偏执的要用 Google 搜索答案，其实这样做并不好，原因：

1. 访问不稳定，延迟，让人焦急
2. 代码都不懂再加上语言障碍，给自己增加了认知负荷。

英文搜索不能丢，因为 Stack Overflow 对于问题的提价更加规范。

访问国内简书、CSDN可以考虑用 简悦 浏览器插件进行美化，用Weavea Hight 插件进行批注，有用内容及时整理到印象笔记类笔记软件。 ==增加链接== 增加 Pocket 插件使用。

2020-2-24 12:36:45

学习需要，进行数据处理使用 NumPy 下载了《使用Python进行数据处理》看到函数部分，一头雾水，还是回来把《笨办法学Python》完成。

输入 `Nee-item` 直接回车，弹出

![mark](http://rsc.waterfree.club/rsc/20200224/ut9lFffPDqnk.png)

在之前的操作过程中也多次出现这个问题，想着必须要解决了。

在百度上搜索，

```powershell
PS C:\Users\lenovo\Desktop> del

位于命令管道位置 1 的 cmdlet Remove-Item
请为以下参数提供值:
Path[0]: test1
Path[1]: Test2
Path[2]: Test3
Path[3]:
PS C:\Users\lenovo\Desktop> ls
```

 发现 `del` 不输入文件名，按 `Enter` 后也会出现这个问题。

大体有感知，但还是不知道：

1. 怎么退出 **命令管道** 赋值
2. 命令管道位置是什么

通常情况下，我们在终端只能执行一条命令，然后按下回车执行，那么如何执行多条命令呢？

管道是一种通信机制，通常用于进程间的通信（也可通过socket进行网络通信），它表现出来的形式将前面每一个进程的输出（stdout）直接作为下一个进程的输入（stdin）。

https://www.jianshu.com/p/9c0c2b57cb73 这里讲的比较详细，已将存在notion中

15 mins 解决问题

## 2020-2-22

在交互式窗口运行Python时经常出现

``` File "<stdin>", line 1``` 的提示，查询后得知，Python有几种方法来读取标准输入的数据。stdin 是一种读取的方式。

学习字典：

- 字典是建立两种数据之间的练习
- 字典与列表不同，字典是无序的

### 2020-2-21

将练习内容同步至 `.gitignore`  （翻译：忽略 git）我是在 Python 的安装文件中编写的程序，我没有必要将 Python 安装包同步到 GitHub, 上传缓慢，让看的的人困惑，甚至影响别人使用，就新建个 `gitignore` 告诉 git，那些是不要同步的。
新建 `.gitignore` 使用文本编辑器打开（不要怀疑就是用文本编辑器打开文件(#^.^#) ），写入不需要同步的文件，同时可用正则表达式不同步某个类型的文件。
- 文件夹名称
- *.××× 后缀为 `xxx` 的文件，如 *.txt ，忽略后缀为 .txt的文件
- ! *.xxx 同步后缀中为 .xxx 文件


参见：

- [使用 git 上传指定的内容（.gitignore的使用）](https://blog.csdn.net/qq_41672008/article/details/89913618)

- [互联网人都该懂点 Git #06 gitignore 和 fork 同步](https://www.baidu.com/s?tn=80035161_2_dg&wd=%E5%93%94%E5%93%A9%E5%93%94%E5%93%A9+gitignore)

**提交错误**

在 github push博客内容时，在里面创建一个目录，然后 git push 的时候，出现报错 "Everything up-to-date"

原因：
1. 没有 git add .
2. 没有 git commit -m "提交信息"
3. 如果上面两个步骤都成功执行，还出现这个错误是因为创建的目录下是空的，目录下必须有文件才能 git push 上传成功。
### 20200215
博客提交过程
  1. ```$ touch 2020-02-14-Blog.md```
跳转到博客目录，新建文章， 注意添加 .md 后缀。

  2. ```$ git add .``` 提交修改内容到缓冲区

  3. ```$ git commit -m "<提交说明>" ``` 说明变化内容，凝练可读 Typo是修改字词。

  4. ```$ git push ``` push本地到仓库的命令

  如果你设置了密码，需要输入密码，但是不会出现密码，正常输入即可

  等待传入，推送成功


**Git Bash 语法说明：**

以提交命令为例：
$ git commit -m "<修改说明>"

同时 -m 部分可以替换（注：连字符与字母之间没有空格）

commit 后面的参数可以为：
- -m 为简短说明；
- --amend 修改提交说明；

push 后面的参数可以为：
- .只提交修改部分的内容
- A 提交全部内容

==待增补== 补充语法说明，改成代码块的形式




### 2020-2-14
拼写错误
- 大小写： print √；Print ×。不像输入验证码不区分大小写，Python对大小写敏感
- 顺序：True √；Ture。汉子序顺并不影响读阅。英文也是。
- 按键失误：number √；nmber ×。
## 准备
### 诚心正意
诚心正意，而后格物致知，而后修齐治平！

诚心正意，是动机。动机需要培养，需要呵护。

黑客是信息时代的手艺人，详见《黑客与画家》。

不同学科有自己特有的思维模式，测绘告诉我分级控制精度，体育告诉进步要适当负荷，周期化自己能力提升。

编程告诉自己自动化思维、Crude思维，自动化思维、学会 if 选择，思维不再线性化。
### 道
老阳文章 ==待增补==
camp101 ===待增补==
### 术
以书籍为主，辅以视频资料，疑难问题自己想和网络搜索。
- 笨办法学Python——主要参考教材
- GitHub入门与实践——熟悉GitHub量化学习，记录学习过程
- Python编程快速上手——交互式学习Python

**说明**：书籍为主，而不是视频。书籍可以方便检索、跳跃，在对应位置做笔记，便于引用，忘了还有迹可循，便于复习。
问题解决不了，看视频，图文教程撰写过程，信息有缺失。

在哪里用就在哪里学，做程序员不知道 GitHub 终归不会有大成就；不做程序员，浸淫在 GitHub 体会协同办公，高效交流。

Python编程快速上手，有很多使用 Python 进行自动化的例子，给 Python 使用寻找出路。没有一本书可以告诉你全部问题，在笨办法学Python中苦恼的问题，些许在这本书就得到了解释，比如说代码块。

网络资源
网络资源不可全信哦，毕竟是没有经过同行评审的。
有些来源更加可靠：
  - Stack Overflow 90%的疑问在这里你都能找到答案，剩下的 10% 可能是拼写错误。
  - 菜鸟教程
## README
一口吃不成胖子，一下学不成编程，记录编程成长路，回头看看一点感动，也是记忆外部化！

[^1]: 