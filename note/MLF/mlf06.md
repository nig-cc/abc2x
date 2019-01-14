 # Theory of Generalization 通用理论
 ## 上节回顾

训练中最有效的选择价值： m(N) 有突破点 k

也就是说猜测 2D 感知器的 m(N) 是多项式级别

## Restriction of Break Point

先来看一下四种类型 m(N) 与 k 的关系

![](/images/gt01.png)

因此，假设 k=2(取最小时)，那么 m(N) 是多少 

![](/images/gt02.png)

可以看到 N>k 时，k 限制了 m(N) 的大小，也就是说影响因素
- 抽样数据集 N
- 突破点 k

那么，如果给定 N 和 k，只要证明 m(N) 的最大值的上界是多项式的，就能用 m(N) 代替 M <-> 机器学习是可行的
 
## Bounding Function

边界函数 B(N,k)：指的是当突破点为 k 的时候，成长函数 m(N) 可能的最大值 

![](/images/gt03.png)

那么，新的目标就是证明 B(N,k) ≤ poly(N)

![](/images/gt04.png)

求解 B(N,k) 的过程十分巧妙
- 当 k=1 时，B(N,1) 恒为 1
- 当 N < k 时，根据`突破点`的定义，很容易得到 B(N,k) = 2^N
- 当 N = k 时，B(N,k) = 2^N-1
- 当 N > k 时，B(N,k) = B(N-1,k) + B(N-1,k-1)

根据递推公式，推导出B(N,K)满足下列不等式(上界满足多项式分布)

![](/images/gt05.png)

代入有突破点的三种成长函数看看

![](/images/gt06.png)

因此，对于2D 感知机，突破点为 k=4，m(N) 的上界是 N^(k-1)

## A Pictorial Proof

对通用 h 来说，E_in 与 E_out 相差 的概率都是有上界的

![](/images/gt07.png)

步骤一

![](/images/gt08.png)

步骤二 

![](/images/gt09.png)

步骤三

![](/images/gt10.png)

总结一下

![](/images/gt11.png)
