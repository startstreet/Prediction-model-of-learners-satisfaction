[TOC]

# 机器学习、深度学习教程汇总

首先，由于最后的产出是**论文形式**的，加上接下来可能要阅读一些论文，为了能看懂论文，最好对机器学习的**基础知识**有一些储备。

接着，有了一定的知识后，就可以借助**Python**实现一些机器学习算法、借助神经网络框架**PyTorch**实现一些神经网络。然后综合这些算法设计出我们的系统（参考一些论文），**阅读论文寻找新思路**对系统进行调优。

## 理论部分

### 1 吴恩达机器学习【视频】

容易上手，包含一些数学公式推导，但编程训练少而且是MATLAB（请看**实战部分第一点**）

（网易云课堂）https://study.163.com/course/introduction/1210076550.htm

### 2 深度学习工程师-吴恩达【视频】

上面的续集，主要是深度学习领域，也就是我们的研究方向，讲了深度卷积、序列模型等等

（网易）https://mooc.study.163.com/smartSpec/detail/1001319001.htm

### 3 台大李宏毅人工智能系列【视频】

听说也是不错的系列视频，包含了线性代数、机器学习等部分（线性代数都学过了，这部分也许能快进或跳过），==入门机器学习可以**吴恩达或李宏毅2选1**==

（网易）https://study.163.com/series/1202814602.htm

（B站）https://www.bilibili.com/video/av59538266

附Github李宏毅学习笔记https://github.com/datawhalechina/leeml-notes，其中**docs/homework附有作业python代码**

### 4 机器学习周志华【书籍】

感觉没有基础会比较难懂，而且有些公式没有详细的推导，于是有了**【南瓜书】**的存在。

[^南瓜书]: 周志华老师的《机器学习》（西瓜书）是机器学习领域的经典入门教材之一，周老师为了使尽可能多的读者通过西瓜书对机器学习有所了解，所以在书中对部分公式的推导细节没有详述，但是这对那些想深究公式推导细节的读者来说可能“不太友好”。github仓库“南瓜书(PumpkinBook)”对西瓜书里比较难理解的公式加以解析，以及对部分公式补充具体的推导细节。

<img src="C:\Users\AstirMoonscape\AppData\Roaming\Typora\typora-user-images\image-20200714153306452.png" alt="image-20200714153306452" style="zoom: 25%;" />

【西瓜书PDF】https://wws.lanzous.com/izN7celj5aj 

【南瓜书】https://datawhalechina.github.io/pumpkin-book/#/

## 实践部分

如果只看理论部分，可能会非常枯燥，所以需要代码来训练巩固

### 1 吴恩达机器学习笔记

Github标星1w多，吴恩达机器学习课程资源（**完整笔记、视频、python作业**），**code目录是吴恩达课程代码的python实现**（因为原课程吴恩达用的是octave）

https://github.com/fengdu78/Coursera-ML-AndrewNg-Notes

### 2 PyTorch学习-莫烦【视频】

很喜欢他的讲课，比较适合入门，但是代码没有过多的解释

（Github博客）https://morvanzhou.github.io/tutorials/machine-learning/torch/

（B站）https://www.bilibili.com/video/BV1Vx411j7kT?from=search&seid=955631354363636993

**【示例源码】**https://github.com/MorvanZhou/PyTorch-Tutorial/tree/master/tutorial-contents

[^注]: 因为莫烦Pytorch教程是很早之前出的，而现在pytorch框架迭代后，视频中的代码有部分已经不适配现在的pytorch版本，所以写代码请参照**【示例源码】**部分进行修改

### 3 Deeplizard《Pytorch神经网络高效入门教程》中字

听说也是国外不错的教程，对张量、面向对象都有直观动画描述。还没看先mark，视频长度比莫烦更长，也许对pytorch会讲的更清楚。

https://www.bilibili.com/video/BV1UE411N7pD?p=2

### 4 PyTorch官方文档-中文

实际编程的时候可以有所参照，讲的很清楚很舒服

https://pytorch.apachecn.org/docs/1.4/ 

### 5  Deep Learning with PyTorch【书籍】

<img src="C:\Users\AstirMoonscape\AppData\Roaming\Typora\typora-user-images\image-20200714161543745.png" alt="image-20200714161543745" style="zoom:25%;" />

貌似是pytorch的官方权威教程，英文版

【PDF】https://wws.lanzous.com/iNcIkelj5hg

【知乎专栏-中文理解】https://zhuanlan.zhihu.com/PyTorch-From-entry-to-abandon

【中文版翻译-进度缓慢】https://tangshusen.me/Deep-Learning-with-PyTorch-Chinese/#/





