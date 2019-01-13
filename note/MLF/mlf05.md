# Training versus Testing 训练 VS 测试
## Recap and Preview 回顾
该流程图中，训练样本D和最终测试h的样本都是来自同一个数据分布，这是机器能够学习的前提

如果 M 是有限的，N 足够大，那么通过演算法 A 任意选择一个 g，都有 E_in ≈ E_out

同时，如果找到一个 g，使得E_in≈0，那么很可能 E_out≈0。

至此，就证明了机器学习是可行的

![](/images/tt01.png)

上四门课的主要内容
- 第一课，机器学习的目的是 g≈f <-> E_out≈0
- 第二课，通过 PLA、Pocket 算法来实现 E_in≈0
- 第三课，学习了填鸭式监督式二元分类问题
- 第四课，通过统计学知识证明了 E_in≈E_out(某些情况下)

这里有两个核心问题
- E_in≈E_out？
- E_in≈0？

![](/images/tt02.png)

上面假设 M 是有限的，那么 M 与这俩个核心问题有什么关系呢？

![](/images/tt03.png)

当 M 很小时
- 霍夫丁不等式 -> E_in≈E_out 
- h 有限时，保证 E_in 足够小的 h 不一定能找到

当 M 很大时
- 霍夫丁不等式 -> E_in 与 E_out 差距可能很大
- h 有很多选择，保证 E_in 足够小的 h 很有可能能找到

这样来看，M 的选择直接影响机器学习的两个核心问题是否被满足

那么，M 无穷大时，是否机器就不可以学习了？

如果我们把无穷大的 M 限定在一个有限的 m 内，问题似乎就解决了，如PLA

![](/images/tt04.png)

## Effective Number of Line

我们先看一下 M 从哪来的？

![](/images/tt05.png)

可以看出来这种做法假设各个 h 之间没有交集，这是最坏的情况

可是实际上往往不是如此，很多情况下，都是有交集的，也就是说 M 实际上没那么大

![](/images/tt06.png)

所以，我们的目的是找出不同 BAD events 之间的重叠部分，也就是将无数个 h 分成有限个类别

如何将无数个 h 分成有限类呢?我们先来看这样一个例子

![](/images/tt08.png)

1 个点有 2 种情况的线

![](/images/tt10.png)

2 个点有 4 种情况的线

![](/images/tt12.png)

3 个点有 4 种情况的线

![](/images/tt13.png)

4 个点有 14 种情况的线

总结一下如下

![](/images/tt14.png)

## Effective Number of Hypotheses

![](/images/tt15.png)

4

![](/images/tt16.png)

5

![](/images/tt17.png)

6

![](/images/tt18.png)

## Break Point

1

![](/images/tt19.png)

2

![](/images/tt20.png)

3

![](/images/tt21.png)

4

![](/images/tt22.png)

5

![](/images/tt23.png)

6

![](/images/tt24.png)

6

![](/images/tt25.png)
