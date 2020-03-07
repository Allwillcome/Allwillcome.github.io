---
`layout: post
title:笨办法学Python
date: 2020-2-21
categories: blog
tags: [学习，黑客]
description: 记录黑客成长路！
---

**记录 Python 学习路**

### README

程序运行有日志，自己学习也要有记录。

记录自己学习 Python 中遇到的问题，

1. 便于自己回头查看；

2. 复盘查看，优化学习过程；

3. 整理成文，分享学习过程

**文章结构**：

- 以日期为三级标题 （便于以后将里程碑设置为二级标题）
  - 在 三级标题内 以时间为节点记录内容

### 02 WEEK 

### 2020-3-7

总结

编程 8 小时（包含学统计时间）

代码 50 hang

2020-3-7 22:26:03

- 用 Python 学编程遇到的问题
  - 英语
  - 代码 和 语法
  - 变量名
  - 统计学知识
  - 方法
    - cheat sheat 纸质笔记，自己看就行，多动脑筋

2020-3-7 22:22:38

- 正则表达式学习
  - https://regex101.com/

2020-3-7 12:22:29

- 给图标增加标签后，不能显示图片
  - 问题描述及解决 https://github.com/AllenDowney/ThinkStats2/issues/121
  - 解决办法，代码一条运行
  - 总结
    - 不要忘记 GitHub ，尤其是作者 GitHub 的 issue
    - 严格按照作者使用的软件甚至是代码格式
    - 问题解决用时： 3 h

2020-3-7 10:53:55

- [Matplotlib](https://matplotlib.org/) 是 python 中的一个 2D 图形库, 它能以各种硬拷贝的格式和跨平台的交互式环境生成高质量的图形, 比如说柱状图, 功率谱, 条形图, 误差图, 散点图等. 其中, matplotlib.pyplot 提供了一个类似 matlab 的绘图框架, 使用该框架前, 必须先导入它.

- Pandas 与 
- pandas Cheat sheet 结合 matplotlib 库，可以将数据已图表的形式可视化，反映出数据的各项特征。

![](https://images2018.cnblogs.com/blog/1295539/201803/1295539-20180320121307556-347978856.png)

2020-3-7 10:04:23

- 在一张图上绘制两个数据集

```python 
import numpy as np
import matplotlib.pyplot as plt
x = np.linspace(0, 2*np.pi, 50)
plt.plot(x, np.sin(x),x,np.sin(2*x))
plt.show()
```

这段代码和前面绘制一个数据集的代码几乎完全相同，只有一点例外，这段代码在调用 `plt.plot()` 的时候多传入了一个数据集，并用逗号与第一个数据集分隔开。

2020-3-7 10:04:18

- 学习 Matplotlib 步骤
  - 学习基本的 matplotlib 术语，尤其是什么是图和坐标轴
  - 始终使用面向对象的接口，从一开始就养成使用它的习惯
  - 用基础的 pandas 绘图开始你的可视化学习
  - 用 seaborn 进行更复杂的统计可视化
  - 用 matplotlib 来定制 pandas 或者 seaborn 可视化
  - <img src="https://mmbiz.qpic.cn/mmbiz_png/fhujzoQe7Tr0qXookOvL2cT5KyyW0ll6aADIkWbuu0ySgzVuwwl3Oj8dgia5jxiaa4s52dhmfFHF5DKSRwZXBjsA/640?wx_fmt=png" style="zoom:25%;" /> 

### 2020-3-6

**代码**

170 lines 

**时间**

7h



2020-3-6 22:04:11

- 注意细节 搜索不能解决问题
  - 在进行 ThinkStats2 的Ch2 练习绘制直方图时，可以出现图，但是没有具体的直方图。搜索一圈之后，没有找到解决办法，想起来自己昨天更改 matplotlib 的默认配置了
  - <img src="http://pics.waterfree.club/20200306221021搜索不能解决问题.jpg" style="zoom:50%;" />
  - 仔细对比，坐标轴果然不一样，左边坐标轴数值太小以至于不能显示

2020-3-6 21:59:14

- %matplotlib
  - %matplotlib具体作用是当你调用matplotlib.pyplot的绘图函数plot()进行绘图的时候，或者生成一个figure画布的时候，可以直接在你的python console里面生成图像

2020-3-6 21:52:04

- [matplotlib 画图中文显示为方框的解决方法_Python_chenjt的博客-CSDN博客](https://blog.csdn.net/q1148013214/article/details/81172446)

2020-3-6 21:24:55

- `os` 模块
  - os 是 operation system （操作系统）的缩写，这个库是对操作系统的封装，自适应 Linux 、Windows等系统。
  - 常见操作
    - os.name——name
    - os.getcwd()——全称应该是'get current work directory'，获取当前工作的目录
    - os.listdir(path)——列出 path 目录下所有的文件和目录名
    - os.chdir(path)——'change dir'改变目录到指定目录
  - ref：[python中os模块简介 - 飞天神猫丶 - 博客园](https://www.cnblogs.com/zxy6/p/11673425.html) 

2020-3-6 21:16:34

- Python 切换工作路径

  - Spyder 的默认工作目录是在  `C:\\Users\\lenovo` , 想要切换，需要用到python的 `os` 模块。

  - ###### 进入 python 控制台，查看工作路径，需要导入 os 包：

    `import os`

  3. 查看工作路径的命令：

      `os.getcwd()`

  4. 修改工作路径的命令：

     `os.chdir("d:\\program")`
     
     ref:不错的 blog [潘高的小站](https://blog.pangao.vip/) 

[Python操作目录，如：获取当前工作目录，获取执行命令的位置，路径拼接，路径拆分，文件重命名，删除文件，复制文件 | 潘高的小站](https://blog.pangao.vip/Python%E6%93%8D%E4%BD%9C%E7%9B%AE%E5%BD%95%EF%BC%8C%E5%A6%82%EF%BC%9A%E8%8E%B7%E5%8F%96%E5%BD%93%E5%89%8D%E5%B7%A5%E4%BD%9C%E7%9B%AE%E5%BD%95%EF%BC%8C%E8%8E%B7%E5%8F%96%E6%89%A7%E8%A1%8C%E5%91%BD%E4%BB%A4%E7%9A%84%E4%BD%8D%E7%BD%AE%EF%BC%8C%E8%B7%AF%E5%BE%84%E6%8B%BC%E6%8E%A5%EF%BC%8C%E8%B7%AF%E5%BE%84%E6%8B%86%E5%88%86%EF%BC%8C%E6%96%87%E4%BB%B6%E9%87%8D%E5%91%BD%E5%90%8D%EF%BC%8C%E5%88%A0%E9%99%A4%E6%96%87%E4%BB%B6%EF%BC%8C%E5%A4%8D%E5%88%B6%E6%96%87%E4%BB%B6/) 

[Python获取时间和日期 | 潘高的小站](https://blog.pangao.vip/Python%E8%8E%B7%E5%8F%96%E6%97%B6%E9%97%B4%E5%92%8C%E6%97%A5%E6%9C%9F/) 

2020-3-6 19:35:55

- 在 windowns 系统上 python 中调用自己写的函数

  ```python
  import sys # 调用 sys 库
  sys.path.append(r"E:\pycharm") # E:\pycharm 替换为自己函数所在目录
  
  ```

  另外， 查看函数的安装路径

  ```python 
  import sys
  sys.path
  ```

  

2020-3-6 13:27:50

- Why Python for statistics?
  - R is a language dedicated to statistics. Python is a genneral-purpose languge with statistics modules. R has more statistical analysis features than Python, and specialized synataxes. However, when it comes to building complex analysis pipelines that mix statistics with e.g image analysis, text mining, or control of a physical experiment, the richness of Python is an invaluable asset.
  - ref:https://scipy-lectures.org/packages/statistics/index.html

2020-3-6 13:18:22

- NA = not available
  -  The weight of the second individual is missing in the CSV file. If we don’t specify the missing value (NA = not available) marker, we will not be able to do statistical analysis.

2020-3-6 13:08:09

- python 中 `\` 是转义字符

  - 输入路径

  ```python
  data = pandas.read_csv('F:\Explore\auto_examples_python10\brain_size.csv',sep=';',na_values=".")
  ```

  运行后，提示

  ```python
  FileNotFoundError: [Errno 2] File b'F:\\Explore\x07uto_examples_python10\x08rain_size.csv' does not exist: b'F:\\Explore\x07uto_examples_python10\x08rain_size.csv'
  ```

  路径是复制粘贴过来的

  - 将文件复制粘贴到桌面

  ```python
   data = pandas.read_csv("C:\Users\lenovo\Desktop\brain_size.csv",sep=';', na_values='.')
  ```

  运行后提示

  ```
  SyntaxError: (unicode error) 'unicodeescape' codec can't decode bytes in position 2-3: truncated \UXXXXXXXX escape
  ```

  - 百度问题 ：在Python中\是转义符，\u表示其后是UNICODE编码，因此\User在这里会报错，在字符串前面加个r表示就可以了

  ```python 
  data = pandas.read_csv("F:/Explore/auto_examples_python10/brain_size.csv",sep=';',na_values=".")
  ```

  问题解决，同样在 上出错误上加上 `r` 同样适用

  ```python 
  data = pandas.read_csv(r"F:\Explore\auto_examples_python10\brain_size.csv",sep=';',na_values=".")
  ```

  将 `\` 换成`/` ,即

  ```python
   data = pandas.read_csv("F:/Explore/auto_examples_python10/brain_size.csv",sep=';',na_values=".")
  ```

  

2020-3-6 11:08:52

viz mode 可视化编程 http://www.codeskulptor.org/viz/

2020-3-6 10:40:51

- **Scratch**是麻省理工学院的“终身幼儿园团队”（Lifelong Kindergarten Group）开发的图形化编程工具，主导开发的针对 5-12 岁儿童的可视化编程语言。只需要使用鼠标，学生就可以编写自己的故事书，动画片或者小游戏。 Scratch 是很好的培养学生的创新力、系统思维和协作的工具。

2020-3-5 17:37:55

- stack
  - ref：
    - [Python中stack(),vstack(),hstack()的用法和区别](https://blog.csdn.net/qq_39521554/article/details/80469666)
    - real

**2020-3-5**

2020-3-5 14:43:15

- 实操 Fraction 函数，使用 for 循环 计算等差数列

2020-3-5 14:10:59

- TensorFlow
  - TensorFlow 是一个端到端开源**机器学习**平台它拥有一个包含各种工具、库和社区资源的全面灵活生态系统，可以让研究人员推动机器学习领域的先进技术的发展，并让开发者轻松地构建和部署由机器学习提供支持的应用。
  - TensorFlow™ 是一个采用数据流图（data flow graphs），用于数值计算的开源软件库。节点（Nodes）在图中表示数学操作，图中的线（edges）则表示在节点间相互联系的多维数据数组，即张量（tensor）http://www.tensorfly.cn/ 。这些数据“线”可以输运“size可动态调整”的多维数据数组，即“张量”（tensor）。张量从图中流过的直观图像是这个工具取名为“Tensorflow”的原因。一旦输入端的所有张量准备好，节点将被分配到各种计算设备完成异步并行地执行运算。
  - ![](http://www.tensorfly.cn/images/tensors_flowing.gif) 
  - ref:[TensorFlow](https://tensorflow.google.cn/) 中国区可以访问，还有公众号
    - [TensorFlow教程系列 |莫烦Python](https://morvanzhou.github.io/tutorials/machine-learning/tensorflow/)

2020-3-5 13:39:44

- 元祖
  - 与列表区别，元组元素不能修改（更加安全），元祖使用小括号，列表使用方括号
  - t = (1,) 单个元祖的定义，在代码后面有个， 这是因为括号()既可以表示tuple，又可以表示数学公式中的小括号，这就产生了歧义，
  - ref：[Python 元祖（Tuple）操作详解](https://www.jb51.net/article/47986.htm)

2020-3-5 13:29:17

[python根据路径导入模块的方法](https://www.jb51.net/article/55840.htm)

2020-3-5 12:55:40

- 安装 Anaconda，提示`NotWritableError: The current user does not have write permissions to a required path` 
- 解决方法：最简单的解决方法就是以管理员身份启动 Anaconda（Anaconda Navigator 或者 Anaconda Prompt）
- ref：[Anaconda报NotWritableError错时解决的方法_](https://blog.csdn.net/qq_29680341/article/details/82917703)

2020-3-5 12:28:48

`conda install -c anaconda cudatoolkit=8.0`

有些包在 conda 默认的 channels 中不包含，比如 cudatoolkit-8.0，cudnn 等，这时只需要在 conda install 指令后加上 - c anaconda 即可。比如要下载 cudatoolkit-8.0，在只需要输入

2020-3-5 12:05:36

- 在社区中学习

  - 配置文件

  - **plotly的在线绘图个人设置**

    **4.1 在线绘图的配置**

    有两种配置方式，

    **方式一：代码配置。**即在绘图代码里面进行配置。在使用plotly绘图之前，添加如下代码即可：

    ```python
    import plotly 
    plotly.tools.set_credentials_file(username='DemoAccount', api_key='lr1c37zw81')
    ```

    **方式二：配置文件配置。**直接修改配置文件，在自己的用户目录下面，找到下面的配置文件，并加以配置，将看到如下内容，自己修改即可。

    ```python
    {
        "username": "DemoAccount",
        "stream_ids": ["ylosqsyet5", "h2ct8btk1s", "oxz4fm883b"],
        "api_key": "lr1c37zw81"
    }
    ```

    ref:[python绘图骚操作之plotly（一）——plotly的基本绘图方式 - 云+社区 - 腾讯云](https://cloud.tencent.com/developer/article/1438008)

2020-3-5 11:45:11

使用 plotly 在线绘图 #API

[plotly----比matplotlib更简单更美观的交互式绘图python库_](https://blog.csdn.net/u010137742/article/details/88851504)



2020-3-5 11:43:25

Plotly is a data science and AI company focused on taking data science out of the lab and into the business. Plotly makes it easy to create, deploy, and share interactive web apps, graphs, and visualizations in any programming language.

ref: https://plot.ly/about-us/

2020-3-5 11:38:56

- Plotly
  - plotly 是一个可交互，基于浏览器的绘图库，主打功能是**绘制在线可交互的图表**, 所绘制出来的图表真的赏心悦目。它所支持的语言不只是 Python，还支持诸如 r,matlab,javescript 等语言。plotly 绘制的图能直接在 jupyter 中查看，也能保存为离线网页，或者保存在 [plot.ly](https://blog.csdn.net/u010137742/article/details/plot.ly) 云端服务器内，以便在线查看。（[Version 4 Migration Guide | Python | Plotly](https://plot.ly/python/v4-migration/#offline-features-plotlyoffline-replaced-by-renderers-framework--html-export) 支持在线版本了）
  - ![](http://upload-images.jianshu.io/upload_images/1068454-4c9c74bfaf105cc8.png)  

早上上数据统计课程，好奇有没有 ”用Python学数据统计“ 的专业书籍，国内只有一本正在翻译的书籍还正在翻译，百度不行，用 google，正好看到了早上，王叔义在 知乎如何学 Python， 提到了 Coursera 、DataCamp，还有经常看大妈公众号中的配图。

![](https://robocrop.realpython.net/?url=https%3A//files.realpython.com/media/Intro-to-Exploratory-Data-Analysis-With-Pandas_Watermarked.81a7d7df468f.jpg&w=480&sig=789fb7504a5df66a3ec5f1677ed5f1ee329d3008)





学习资源

* [Basic Statistics | Python/v3 | Plotly](https://plot.ly/python/v3/basic-statistics/#import-data) plotly 关于 Statistics 的介绍
* [Statistics with Python | Coursera](https://www.coursera.org/specializations/statistics-with-python) Coursera 的 MOOC，学时 8 周
* [3.1. Statistics in Python — Scipy lecture notes](https://scipy-lectures.org/packages/statistics/index.html) 附带操作代码
* [statistics --- 数学统计函数 — Python 3.8.2 文档](https://docs.python.org/zh-cn/3/library/statistics.html) 官方 statistics 模块介绍
* [Python Tutorials – Real Python](https://realpython.com/) 
* [Python Tricks: The Book – Real Python](https://realpython.com/products/python-tricks-book/) 每天一个代码小游戏
* [Introduction to Exploratory Data Analysis | Python](https://campus.datacamp.com/courses/statistical-thinking-in-python-part-1/graphical-exploratory-data-analysis?ex=1) DataCamp 的 Python 课程

**2020-3-4**

3 h，200 lines 代码
2020-3-4 17:10:05

- 学习 scipy interpolate 的使用
  - [Interpolation (scipy.interpolate) — SciPy v1.4.1 Reference Guide](https://docs.scipy.org/doc/scipy/reference/tutorial/interpolate.html) 
- 学习 Matplotlib 
  - 学习过程中遇到，`TypeError: 'numpy.ndarray' object is not callable ` 重启 Spyder 后问题解决。
  - [Matplotlib 教程 |中文翻译](https://liam.page/2014/09/11/matplotlib-tutorial-zh-cn/)
  - [Matplotlib: Python plotting — Matplotlib 3.1.3 documentation](https://matplotlib.org/index.html)

**2020-3-3** 

2020-3-3 20:34:10

**总结**

代码 200 lines

**时间**

3 h

学习 numpy 

2020-3-3 20:21:34

**Anaconda切换国内镜像源**

清华镜像源：

[https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/](https://link.zhihu.com/?target=https%3A//mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/)

​    (1) 打开Anaconda Prompt，执行命令：

```text
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
```

​    (2) 执行命令：

```text
conda config --set show_channel_urls yes
```

​    (3) 此时C:\Users\Administrator\下已经生成配置文件：.condarc，内容如下：

![img](https://pic3.zhimg.com/v2-0b93d391477b8dbcd415a6ed42aad2f2_b.jpg)

删除第3行，保存；

(4) 查看是否生效，执行命令：

```text
conda info
```

关注channel URLs下的内容：



![img](https://pic1.zhimg.com/v2-99803cf8ab3eedfb325395037ad85ef4_b.jpg)



​    (5) 测试一下，安装爬虫包 scrapy，执行命令：conda install scrapy

2020-3-3 18:03:59

**Ch 4.3 Array-Oriented Programming with Arrays **

数组导向编程

2020-3-3 18:39:39

**Anaconda大法好**

比如输入一下命令

```python
import matplotlib.pyplot as plt
%matplotlib inline
plt.style.use('ggplot')

plt.plot(X, Y, marker='.', color='blue', linestyle='none')
```

调用的函数,有这么多，只下载 python 3 怎么知道其他安装包在不在

```python
Traceback (most recent call last):

  File "<ipython-input-193-fda2b5acf644>", line 1, in <module>
    plt.plot(X, Y, maker= '.', color = 'blue',makersize = 20,linestyle='none')

  File "D:\Program\Anaconda-20-3-1\lib\site-packages\matplotlib\pyplot.py", line 2795, in plot
    is not None else {}), **kwargs)

  File "D:\Program\Anaconda-20-3-1\lib\site-packages\matplotlib\axes\_axes.py", line 1666, in plot
    lines = [*self._get_lines(*args, data=data, **kwargs)]

  File "D:\Program\Anaconda-20-3-1\lib\site-packages\matplotlib\axes\_base.py", line 225, in __call__
    yield from self._plot_args(this, kwargs)

  File "D:\Program\Anaconda-20-3-1\lib\site-packages\matplotlib\axes\_base.py", line 405, in _plot_args
    seg = func(x[:, j % ncx], y[:, j % ncy], kw, kwargs)

  File "D:\Program\Anaconda-20-3-1\lib\site-packages\matplotlib\axes\_base.py", line 312, in _makeline
    seg = mlines.Line2D(x, y, **kw)

  File "D:\Program\Anaconda-20-3-1\lib\site-packages\matplotlib\lines.py", line 404, in __init__
    self.update(kwargs)

  File "D:\Program\Anaconda-20-3-1\lib\site-packages\matplotlib\artist.py", line 974, in update
    ret = [_update_property(self, k, v) for k, v in props.items()]

  File "D:\Program\Anaconda-20-3-1\lib\site-packages\matplotlib\artist.py", line 974, in <listcomp>
    ret = [_update_property(self, k, v) for k, v in props.items()]
```



2020-3-3 18:05:33

- [ meshgrid](https://baike.baidu.com/item/meshgrid/3794127?fr=aladdin) 
  - 是MATLAB （一款应用程序） 中用于生成网格采样点的函数，在使用 MATLAB 进行 3D 图形绘制方面有着广泛的应用。
  - <img src="https://img-blog.csdn.net/20180809111254714?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2xsbHh4cTE0MTU5MjY1NA==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70" style="zoom:33%;" />
  - **注意** ：一点就是meshgrid虽然生成了一个坐标矩阵，但是这个矩阵每个元素对应的索引和图中实际的坐标并不是完全对应的，比如说坐标矩阵中的索引[0，0]的位置的元素为（x，y）绘制的点是在（x，y）而不是（0，0）
  - ref:  [numpy.meshgrid()理解_Python_lllxxq141592654的博客-CSDN博客](https://blog.csdn.net/lllxxq141592654/article/details/81532855)

2020-3-3 17:50:01

**Ch 4.2 Universal Functions： Fast Element-Wise Array Funcations**

（通用函数：快速点对点数组函数）

- 一些简单的函数做快速的向量化封装，输入是一个以上的标量，输出也是一个以上的标量。很多 ufuncs 都是点对点的
- `sqrt`  是求平方根；`exp` 是 e 的平方

2020-3-3 17:35:25

**Ch 4.1 The Numpy ndarray （多维数组对象）**

- 完成
  - 1 Creating ndarrays
  - 2 DataTypes for ndarrays 
  - 3 Arithmetic withNumpy Arrays （ 数组计算）
  - 4 基本的索引和切片
  - 5 Boolean Indexing （布尔索引）
  - 6 Fancy Indexing （花式索引）
- 待解决

- [ ] 花式索引
- [ ] 元祖
- [ ] Transposing Arrays and Swapping Axes (数组转置和轴交换)





2020-3-3 13:37:18

**jupyter 打开.ipynb 文件**

​	确保安装 jupyter

 1. 在命令行进入 存放 ipynb 文件所在 目录

 2. 输入命令 `jupyter lab`

 3. 自动弹出

    ref：[jupyter如何打开.ipynb文件？_开发工具_笨笨的静静-CSDN博客](https://blog.csdn.net/lj2048/article/details/100880199) 

2020-3-3 12:11:14

**使用 powershell 批量改文件名 ** 

批量改文件擴展名

需求：將D盤For PS文件夾下的所有的txt文件改爲html文件，即.txt改爲.html

 ```powershell
get-childItem 'D:\For PS' *.txt | rename-item -newname { $_.name -replace '\.txt','.html' } 
 ```

備註：由於replace的模式匹配字符串參數支持正則表達式，'.txt'要轉義成'\.txt'。

###### 批量爲文件加前綴

需求：將D盤For PS文件夾下的所有的txt文件加上一個“Test_”的前綴

1. cd 'D:\For PS' 
2. get-childItem -r *.txt | rename-Item -newname{'Test\_'+$\_.name} 

**2020-3-3 12:03:40**

查看 powershell 的命令别名

​	1. 打开 powershell ，输入`alias`

 2. ```powershell
    echo -> Write-Output
    dir -> Get-ChildItem
    rni -> Rename-Item
    ```

**2020-3-3 11:00:08**

 pip 安装 Erro 13

​	Could not install packages due to an EnvironmentError: [Errno 13] 

`	pip install django-ckeditor --user` 可以解决

**2020-3-3 10:54:11** 

在 powershell 中输入`pip show xxx`（xxx，需查看的包名）

**2020-3-3 10:48:23**

**查看安装包命令** 

\1. Start 一个 command prompt
\2. 找到电脑中已经安装的 Python 位置：（where 命令只能在 cmd 中）

```cmd
where python
```



```cmd
pip list <or> pip freeze
```

**ref:** [如何查看Python 安装位置以及已经安装的库_Python_JennyChen66的博客-CSDN博客](https://blog.csdn.net/JennyChen66/article/details/78487228/) 

**2020-3-3 10:41:21**

Typora 中有一个选项是`./${filename}. assets` ，怎么理解？

直接搜索没有选项；分开搜索 `./${filename}`、 `assets` .

- 关于 `assets` 的英文就是 “资产” 、“有用的东西”
  - assets：一般存放开发过程中自己写的静态资源（image, css, js 等，如：shop.css, car.png, roomListUtil.js）
    static：存放第三方静态资源（jquery.js, bootstrap.css 等），这里的资源一般是直接引用，当打包编译后 assets 中的静态资源也会编译到 static 目录下，这样原来引用 static 资源的地址也不用改变。
  - ref：[assets在前端开发项目中的含义是什么_J-CSDN博客](https://blog.csdn.net/tsingsn/article/details/75313528) 
- **${filename} 用法**
  - #是去掉左边 （在键盘上 #在 ${} 之左边）
  - % 是去掉右边（在键盘上 % 在 ${} 之右边）
  - % %：从左边数第一条，从右边数最后一条
  - % ：  从右边数第一条，从左边数最后一条
  - ref: [${filename}用法一：${file内部的#%的匹配方式} - wqbin - 博客园](https://www.cnblogs.com/wqbin/p/11597700.html) 

**2020-3-2**

**总结** 

200 行代码

- 基本顺利，环境变量还是很重要的概念
- 写入权限

2020-3-2 21:49:56

在 python 中可以直接使用

a, b = b, a

2020-3-2 21:10:21

Python的对象通常都有属性(其它存储在对象内部的Python对象)和方法(对象的附属函数可以访问对象的内部数据) .

2020-3-2 20:50:52

**搜索不能代替思考**

在阅读 《阅读 Python 进行数据分析》时。阅读书上内容

> 阅读对象的类型很重要，最好能让函数可以处理多种类型的输入。你可以用 isinstance 函数检查对象是某个类型的实例：
>
> In [ ]: a =
>
> In [ ]: isinstance(a, )
>
> Out[ ]: True

直接在 Python 37 IDL 中按照书本输入

```python
>>> a =
SyntaxError: invalid syntax
```

文档先后对照，书中没有复制，但是应该赋值

```python
>>> a = 10
>>> isinstance(a,10)
Traceback (most recent call last):
  File "<pyshell#6>", line 1, in <module>
    isinstance(a,10)
TypeError: isinstance() arg 2 must be a type or tuple of types
```

按照在IDLE 中函数提示

![image-20200302210454370](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20200302210454370.png)

```python
>>> isinstance(a,int)
True
>>> isinstance(a,float)
False
```



2020-3-2 19:42:57

通常情况下,许多文件系统操作的命令都有一个与命令提示符CMD中的别名,帮助用户猜测命令的功能，如下：

```powershell
Name  Definition
----  ----------
cli   Clear-Item
clp   Clear-ItemProperty
copy  Copy-Item
cp    Copy-Item
cpi   Copy-Item
cpp   Copy-ItemProperty
del   Remove-Item
erase Remove-Item
gi    Get-Item
ni    New-Item
```





2020-3-2 17:55:29

升级 pip 命令

```powershell
python -m pip install --upgrade pip
```

2020-3-2 17:51:34

例如，使用豆瓣源来安装jieba包
 `pip install jieba -i https://pypi.douban.com/simple`

其他镜像源

阿里云 http://mirrors.aliyun.com/pypi/simple/
中国科技大学 https://pypi.mirrors.ustc.edu.cn/simple/
豆瓣 http://pypi.douban.com/simple
中国科学院 http://pypi.mirrors.opencas.cn/simple/
清华大学 https://pypi.tuna.tsinghua.edu.cn/simple/

ref:[pip国内镜像源配置_Python_abcque的专栏-CSDN博客](https://blog.csdn.net/zhoulinshijie/article/details/87974824) 

2020-3-2 17:37:55

![](http://pics.waterfree.club/20200302174206Python中文.png)

![](F:\Blog\Allwillcome.github.io\_posts\20200302173702Sheban.png)

2020-3-2 16:44:14

142 lines

**继承与合成** 

解决代码复用问题。继承可以让你在基类里遗憾父类的功能，**合成**是利用模块和别的类中的函数调用。

2020-3-2 16:29:10

python 中函数的调用在函数背后应该有 `()` , 如 `son.implicit()` 可以调用，`son.implicit()` 不能调用。

2020-3-2 15:49:22

父类和子类有三种交互方式：

1. 子类的动作完全等同父类的动作 隐式继承（implicit inheritance）
2. 子类的动作完全覆盖父类的动作 显示覆盖 （override inheritance）
3. 子类的动作部分替换父类的动作 替换 （altered）

---

### 01 Week 总结

2020-2-24 **→** 2020-3-1 

**用时**：

36.5 h（4 + 5 +5 +3 + 7 + 4.25 + 6.4）

**收获**：

1. 书写、阅读 200 行代码不再恐惧
2. 丰富代码运行过程中报错的解决方法
   1. 放置问题，补充基本知识
   2. 思考问题的本质，变化搜索问题的角度
   3. 寻求朋友的帮助
3. 了解 Python 和电脑基本知识
   1. 类与对象的区别
   2. 根目录、绝对路径与相对路径
   3. 环境变量
   4. 项目骨架
   5. 在 Windows 上 Python 多版本的安装与运行

学习日志： [The-Journey-of-Learn-Pthon](http://www.waterfree.club/2020/03/01/2020-02-14-The-Journey-of-Learn-Pthon/)

**改进**：

1. 笨办法学 Python，严格按照书上指导，书写代码，运行程序

2. 抑制好奇心，专注当前问题解决

   

### 2020-3-1 

**任务完成**：

- 成功运行 ex43.py 大战哥顿人逃生小游戏
- 对程序进行批注，理解程序
- 理解类与对象

**编程用时：**

7 h

**待改进**：

- 更耐心对不懂程序进行批注
- 多动手编写程序，代码
- 提升效率



2020-3-1 20:14:47

- 问题描述：Typora 官方文档中说可以自动上传拖拽到文件中的图片，自己下载 PicGo 并在 Typora 中进行配置之后，无法自动上传。
  - ![](http://pics.waterfree.club/20200301TyporaImageConfigure.png)
  
- 已经做努力：
  - 以管理员身份打开 Typora 以及 PicGo
  - ![img](http://pics.waterfree.club/20200301202314验证图片上传.png)
  - 查询官网
    - If you use, custom command, and after clicking “Test Uploader” button in preferences panel, and its console output is Garbled characters, you may try to force the process to use UTF8 encoding, by prepending `@chcp 65001 >nul & cmd /d/s/c `before your custom command.
    - 彩云小译翻译：如果您使用，自定义命令，并在首选项面板中单击“ Test Uploader”按钮后，其控制台输出为含糊字符，您可以通过在自定义命令之前预置@chcp 65001 nul & cmd / d / s / c，尝试强制进程使用 UTF8编码。

2020-3-1 17:07:01

**注释**

- 帮助别人理解自己的代码
  - 帮助明天的自己理解自己今天写的代码
- 帮助自己理解别人的代码
  - 写注释，让自己拉近观察代码的细节

2020-3-1 15:24:35

类的好处

- 方便复用
- 方便扩展
- 方便维护

类就像是**基因的制造图纸**，

在 Python 中，一个对象的特征也成为属性（attribute）。它具有的行为也称为方法（method）

**结论：对象 = 属性（特征） + 方法（行为）** 

最后我们用以下代码，让机器开始造猪

```python
pig1 = Pig('猪')  #实例化，相当于怀孕
```

[如和理解 Python 的类与对象](https://www.zhihu.com/question/27699413)



2020-3-1 15:17:27

[python 中类和对象的使用 - 简书](https://www.jianshu.com/p/4b1f9257a2f2)

2020-3-1 14:37:53

- math 函数的引用

- 问题

  - 如何使用 Python 的 `math` 模块？

- 所做尝试

  - 尝试查阅 Python 的文档

  - ```powershell
    FUNCTIONS
        acos(...)
            acos(x)
    
            Return the arc cosine (measured in radians) of x.
    
        acosh(...)
            acosh(x)
    ```

  - [Python 中 math模块常用的方法整理](https://www.cnblogs.com/666gang/p/10952421.html) 

- 归纳总结

  - 查询网络教程
  - 更换数据库
  - 参考错误提示
  - 更换 Python 版本

- 结果：`math.`

2020-3-1 11:36:47

- 问题记录

  - 从 GitHub 上下载 ex43.py 习题，使用Python2.0 进行运行，没有报错，出现以下代码：

  ```powershell
  The Gothons of Planet Percal #25 have invaded your ship and destroyed
  your entire crew.  You are the last surviving member and your last
  mission is to get the neutron destruct bomb from the Weapons Armory,
  put it in the bridge, and blow the ship up after getting into an
  escape pod.
  
  
  You're running down the central corridor to the Weapons Armory when
  a Gothon jumps out, red scaly skin, dark grimy teeth, and evil clown costume
  flowing around his hate filled body.  He's blocking the door to the
  Armory and about to pull a weapon to blast you.
  >
  
  ```

  只有命令提示符，不知道输入什么信息。都是英文，感觉无从下口，决定重新返回代码，关键词定位。运行代码提示为 `You're running down the central corridor` ,在源代码中找到，`CentralCorridor` 

  ![2020030111Python43ex](http://pics.waterfree.club/2020030111Python43ex.jpg)

**2020-3-1 11:08:10**

代码运行无果，百度无法搜谷歌，在 GitHub 上，*Learn Python the Hard Way* ，包含 Python2.0， 与Python3.0，而且知道通过查看仓库`git log` 复原学习过程。

> All the codes are written in both Python2(2.7.5) and Python3(3.3.2).
>
> The best way to check my solution step by step is to use `git log` command. For instance,
>
> ```
> $ git log -p Python2/ex04.py
> ```
>
> Alternatively you can browse the history of any file on GitHub to see the change of it.
>
> If you got a better answer, welcome to comment the code and share your version!

ref : [wzpan/Learn-Python-The-Hard-Way: My answer for the book Learn Python The Hard Way](https://github.com/wzpan/Learn-Python-The-Hard-Way) 

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

[^2.29.13]: [不用装双系统，直接在 Windows 上体Linux：Windows Subsystem for Linux - 少数派](https://sspai.com/post/43813) 

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

[^1]: [YAML语法 ——阮一峰](http://www.ruanyifeng.com/blog/2016/07/yaml.html)

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