# Learning to Answer Yes/No 分辨是非 -> 二元分类问题

## 上节回顾

根据模型 H，使用演算法 A，在训练样本 D 上进行训练，得到最好的 h，其对应的 g 就是我们最后需要的机器学习的模型函数，一般 g 接近于目标函数 f

## Perceptron Hypothesis Set 感知器假设集
信用卡发放问题描述

![信用卡发放问题描述](/images/yn01.png)

那么我们可以用什么样的假设集呢？-> 感知机模型的假设

![感知机模型](/images/yn02.png)

感知机假设的向量形式

![假设简化](/images/yn03.png)

感知机假设长什么样呢？
- 特征向量 x： 空间中的点
- 标签 y： o(+1)， x(-1)
- 假设 h：线 -> 正类在一边，负类在另一边

![二维可视化](/images/yn04.png)

感知器 <-> 线性分离器

## Perceptron Learning Algorithm 感知器学习算法
那么我们如何从 H 中选择 g?
- 我们要的是：g ≈ f（f 未知时很难做到）
- 几乎可能：g ≈ f on D(理想时 g()=f(x)=y )
- 困难：H 无穷大时
- 思路：从一些 g 开始，在 D 上不断改正错误

![算法思路](/images/yn05.png)

感知机学习算法 -> 从一些 g 开始，在 D 上不断[改正错误](/note/SC/向量加法.md)，直到所有的点都完全分类正确

![PLA 模型](/images/yn06.png)

承认错误是成功的一半

PLA的实际实现 -> 循环 PLA

![CyclicPLA](/images/yn07.png)

图解 PLA 修正过程(分割线垂直 w_t)：

![修正01](/images/xz01.png) ![修正02](/images/xz02.png) ![修正03](/images/xz03.png)
![修正04](/images/xz04.png) ![修正05](/images/xz05.png) ![修正06](/images/xz06.png)
![修正07](/images/xz07.png) ![修正08](/images/xz08.png) ![修正09](/images/xz09.png)
![修正10](/images/xz10.png) ![修正11](/images/xz11.png) 

关于 PLA 的一些疑问
- 算法会终止(没有错误)吗？
    - 自然循环时？
    - 随机循环时？
    - 其他变种？
- 学习(g ≈ f)可能吗？
    - on D，如果终止，那么应该可能
    - 在 D 以外呢？
    - 如果不终止呢？
 
## Guarantee of PLA -> 经过足够多次修正后，任何 PLA 的变种都会终止

线性可分的定义

![线性可分](/images/yn08.png)

那么为啥`线性可分`，PLA 就会终止呢？

- 线性可分 <-> 存在一个完美的 w_f，使得所有的点都完全分类正确
- 证明 w_t 越来越[接近](/note/SC/向量内积.md) w_f，且对于任意点成立

![内积](/images/yn09.png)

- 证明 w_t [长度](/note/SC/向量大小.md)不会增长太快
	
![长度](/images/yn10.png)

- 推出迭代次数 T 是有上界的

### 推导过程

假设条件描述

![假设条件](/images/platd01.png)

这意味着两件事
- 基于上述不等式左边(实际上是两向量的 cos)不大于 1，所以迭代次数 T 不大于一个具体值，意味着迭代会结束
- w_t 和 w_f 的角度在逐渐减少，说明w_t 在逐渐靠近 w_f，意味着解决问题的方向是对的

下面是证明过程

对于 w_t 有：

![w_t](/images/platd02.png)

对于 ||w_t|| 有：

![w_t长度](/images/platd03.png)

在这时，先给出一个定义

![定义](/images/gpla06.jpg)

因此，迭代次数可以表示如下

![迭代次数](/images/gpla05.png)

结论：迭代次数 T 是有上界的

## Non-Separable Data 非线性可分数据
PLA 总结 - 只要线性可分并且错误都被更正，就会有
- w_f 与 w_t 的内积增长较快；w_t 的长度增长较慢
- w_t 越来越趋近 w_f（终止时），意味着分割线越来越正确

实际上，可以推广到任意纬度

然而
- 我们基于线程可分的假设来终止迭代
- 并不确定知道需要多久 PLA 才会终止迭代 

![PLA总结](/images/yn11.png)

对于非线性可分的情况，我们可以把它当成是数据集 D 中掺杂了一下 noise，机器学习流程是这样的：

![流程](/images/yn12.png)

这种情况下，我们找不到完美的线，但可以找一条更好的线使得在数据集 D 上错误最少 - NP-hard 问题

![NP-hard](/images/yn13.png)

那怎么办呢？

在修正错误(随机)的线时，我们假设可以遇到一条还不错的线 - Packet Algorithm
- 不确定什么时候终止
- 找到还不错的线就停止

![Packet Algorithm](/images/yn14.png)

## 下一课

[Types of Learning](/note/MLF/mlf03.md)
