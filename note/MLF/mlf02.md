# Learning to Answer Yes/No 分辨是非
## Perceptron Hypothesis Set 感知器假设集
信用借贷问题描述

![信用借贷问题描述](/images/yn01.png)

信用借贷模型

![信用贷款模型](/images/yn02.png)

h(x) 的表达式做如下变换：

![h(x)简化](/images/yn03.png)

h(x) 二维可视化：

![h(x)二维可视化](/images/yn04.png)

## Perceptron Learning Algorithm 感知器学习算法
算法思路

![算法思路](/images/yn05.png)

PLA 模型
- 目标 -> 从 h(x) 找到 g，使得 g ≈ f(**未知**)
- 思想 -> 随意取一条线，然后根据错误点进行修正([向量加法](/note/SC/向量加法.md))，直到所有的点都完全分类正确

![PLA 模型](/images/yn06.png)

Cyclic PLA 模型

![Cyclic PLA 模型](/images/yn07.png)

图解 PLA 修正过程：

![修正01](/images/xz01.png) ![修正02](/images/xz02.png) ![修正03](/images/xz03.png)
![修正04](/images/xz04.png) ![修正05](/images/xz05.png) ![修正06](/images/xz06.png)
![修正07](/images/xz07.png) ![修正08](/images/xz08.png) ![修正09](/images/xz09.png)
![修正10](/images/xz10.png) ![修正11](/images/xz11.png) 

## Guarantee of PLA PLA的保证
线性可分

![线性可分](/images/yn08.png)

PLA 的终止条件，就是 D 是线性可分。这样对于任意点存在 $w_{f}$ 使得 $y_{n}$ = sign($y_{n}$^T$y_{n}$)，[内积](/note/SC/向量内积.md)越大表示越接近

![内积](/images/yn09.png)

还得看看[向量长度](/note/SC/向量大小.md)相差大不大
	
![大小](/images/yn10.png)

也就是说，迭代次数 T 是有上界的

![定义](/images/gpla06.jpg)

![迭代次数](/images/gpla05.png)

## Non-Separable Data 非线性可分数据
PLA 总结

![PLA总结](/images/yn11.png)

对于非线性可分的情况，我们可以把它当成是数据集 D 中掺杂了一下 noise，机器学习流程是这样的：

![流程](/images/yn12.png)

NP-hard 问题

![NP-hard](/images/yn13.png)

Packet Algorithm

![Packet Algorithm](/images/yn14.png)
