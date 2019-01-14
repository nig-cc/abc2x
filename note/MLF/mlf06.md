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
 
## Bounding Function: Basic Cases

边界函数 B(N,k)：指的是当突破点为 k 的时候，成长函数 m(N) 可能的最大值 


那么，新的目标就是证明 B(N,k) ≤ poly(N)

## Bounding Function: Inductive Cases

## A Pictorial Proof
