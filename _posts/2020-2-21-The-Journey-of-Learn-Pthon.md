---
layout: post
title: 笨办法学Python
date: 2020-2-21
categories: blog
tags: [学习，黑客]
description: 记录黑客成长路！
---

**记录 Python 学习路**

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
