# Feasibility of Learning 机器学习可行性
## Learning is Impossible 似乎不可能

根据不同特征进行分类，可以得到不同的结果

![分不准](/images/kx101_.png)

在已知数据 D 上，g≈f 成立；在 D 以外的未知数据上，g≈f 不一定成立

![局限](/images/kx102_.png)

没有免费午餐(No Free Lunch)定理 - 在D以外的数据中更接近目标函数似乎是做不到的，只能保证对D有很好的分类结果

![局限解答](/images/kx103_.png)

一个学习算法比另一个算法更“优越”，只是针对特定的问题，先验信息，数据的分布，训练样本的数目，代价或奖励函数等

结论：**在训练集 D 以外的样本上，机器学习的模型是很难，似乎做不到正确预测或分类的，除非加上一些假设条件**

## Probability to the Rescue 假设可能性
推断罐子中橙色珠子的概率问题

![bin题设](/images/kx201_.png)

抓一把珠子，问**样本中橙色珠子的概率**与**样本外橙色珠子的概率**近似吗？

![问题描述](/images/kx202_.png)

问题思考，极有可能近似

![问题思考](/images/kx203_.png)

用数学公式表示如下

![不等式](/images/kx204_.png)

 显然，当 N 足够大时，可以根据**已知** `v` 推断**未知** `u`

![推断](/images/kx205_.png)

## Connection to Learning 转化到机器学习
如果样本 N 够大，且是独立同分布的，那么就可以根据**样本中 h(x)≠f(x) 的概率**来推断**样本外 h(x)≠f(x) 的概率**

![推断](/images/kx300_.png)

加上元件，抽样中橙球的概率理解为样本数据集 D 上 h(x) 错误的概率，以此推算出在所有数据上 h(x) 错误的概率


![加上元件](/images/kx301_.png)

公式保证

![公式保证](/images/kx302_.png)

验证一个 h
![验证h](/images/kx303_.png)

验证一个 h 流程

![验证流程](/images/kx304_.png)

## Connection to Real Learning 转化到实际学习

出现多个 h 

![多个h](/images/kx401_.png)

抛硬币游戏

![抛硬币游戏](/images/kx402_.png)

不好的数据和标签

![不好的数据和标签](/images/kx403_.png)

对多个 h 来说不好的数据 

![抛硬币游戏](/images/kx404_.png)

不好的数据的边界

![抛硬币游戏](/images/kx405_.png)

统计流程

![抛硬币游戏](/images/kx406_.png)


