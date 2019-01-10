# Types of Learning 机器学习的分类
## Learning with Different Output Space Y 基于输出空间
- 二元分类和多元分类都属于分类问题，它们的输出都是离散值
- 输出是连续的问题属于回归问题
- 结构化学习的输出空间包含了某种结构在里面，它的一些解法通常是从多分类问题延伸而来的，比较复杂

![输出分类](/images/sclx.png)

## Learning with Different Data Label y 数据标签
- 如果我们拿到的训练样本 D 既有输入特征 x，也有输出 y，那么我们把这种类型的学习称为监督式学习
- 与监督式学习相对立的另一种类型是非监督式学习。非监督式学习是没有输出标签 y 的
  - 聚类（clustering）问题，比如对网页上新闻的自动分类
  - 密度估计，比如交通路况分析
  - 异常检测，比如用户网络流量监测
- 半监督式学习就是说一部分数据有输出标签 y ，而另一部分数据没有输出标签 y
- 增强学习中，我们给模型或系统一些输入，如果反馈结果良好，更接近真实输出，就给其正向激励，如果反馈结果不好，偏离真实输出，就给其反向激励

![标签分类](/images/bqfl.png)

## Learning with Different Protocol f 映射
- Batch Learning 一次性拿到整个 D
- Online 根据数据一个个进来，同步更新我们的算法
- Active Learning 让机器具备主动问问题的能力

![映射分类](/images/ysfl.png)
## Learning with Different Input Space X 输入空间
- concrete features 具体特征
- raw features 元特征
- abstract features 抽象特征

将一些抽象的特征转换为具体的特征，是机器学习过程中非常重要的一个环节

![输入分类](/images/srfl.png)
