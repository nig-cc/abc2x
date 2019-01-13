# The Learning Problem 机器学习相关问题
## What is Machine Learning 什么是机器学习 -> 使用数据逼近目标

从学习引入机器学习
- 学习 - 人类通过`观察`，积累`经验`，掌握某项`技能`
- 机器学习 - 机器通过对大量的数据`训练`，发现事物`规律`，获得某种解决问题的`能力`

![从学习到机器学习](/images/jqxx00.png)

那么，这种能力代表什么？-> 某些性能度量的增益

![能力](/images/jqxx01.png)

为什么使用机器学习？ -> 解决复杂问题的替代路径

![为什么使用机器学习](/images/jqxx02.png)

有哪些路径？-> 授机器以鱼，不如授机器以渔

![授之以渔](/images/jqxx03.png)

机器学习的关键条件？-> 帮助决定是否使用机器学习
- 事物本身存在某种潜在规律
- 某些问题难以使用普通编程解决
- 有大量的数据样本可供使用

![关键本质](/images/jqxx04.png)

## Applications of Machine Learning 机器学习的应用领域 -> 几乎任何领域
- 食、衣、住、行

![食、衣、住、行](/images/jqxx05.png)

- 教育

![育](/images/jqxx06.png)

- 娱乐

推荐系统

![关键本质](/images/jqxx07.png)

机器是怎么学习我们的偏好的？

![关键本质](/images/jqxx08.png)

- 金融、医药、法律

## Components of Machine Learning 机器学习的组成部分 -> `A` takes `D` and `H` to `g`

假设一个信用卡发放问题 -> 怎么发放信用卡对银行有利？

![信用卡发放](/images/jqxx09.png)

公式化这个学习问题
- 输入 `X`
- 输出 `Y`
- 目标函数 `f` <- 未知
- 训练样本 `D`
- 假设集(H)中最好假设 `g` <- 目标: `g` ≈ `f`

![组成部分](/images/jqxx10.png)

信用卡发放评估的学习流程 

![学习流程](/images/jqxx11.png)

合适的 g 是什么样子的？-> 学习模型

![学习模型](/images/jqxx12.png)

机器学习的评估定义 -> 从数据中学习`g`，使得 `g` ≈ `f`

![评估定义](/images/jqxx13.png)

## Machine Learning and Other Fields 机器学习与其他领域

- 机器学习与数据挖掘的关系 -> 在现实中很难区分

![数据挖掘](/images/mldm.png)

- 机器学习与人工智能的关系 -> 是实现 AI 的一个可能路径

![人工智能](/images/mlai.png)

- 机器学习与统计学的关系 -> 有很多对机器学习又用的工具

![统计学](/images/mlst.png)

## 下一课

[Learning to Answer Yes/No](/note/MLF/mlf02.md)
