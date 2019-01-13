# Types of Learning 机器学习的分类
## 上节回顾

    A(`PLA`) takes D(`线性可分) and H（`感知器`） to get g(`假设`)

## Learning with Different Output Space Y 基于输出空间

信用贷款审核问题 - 二元分类问题

![输出分类](/images/type01.png)

其他二元分类问题

![其他二元分类问题](/images/type02.png)

硬币识别问题 - 多元分类问题

![硬币识别问题](/images/type03.png)

患者康复预测问题 - 回归问题

![患者康复预测问题](/images/type04.png)

序列标记问题 - 结构化学习

![序列标记问题](/images/type05.png)

总结
- 二元分类和多元分类都属于分类问题，它们的输出都是离散值
- 输出是连续的问题属于回归问题
- 结构化学习的输出空间包含了某种结构在里面，它的一些解法通常是从多分类问题延伸而来的，比较复杂

![总结1](/images/type06.png)

## Learning with Different Data Label y 基于数据标签
硬币识别(知道标签) - 监督式学习

![硬币识别1](/images/type07.png)

硬币识别(不知道标签) - 非监督式学习

![硬币识别2](/images/type09.png)

其他非监督式学习

![其他非监督式学习](/images/type10.png)

硬币识别(知道部分标签) - 半监督式学习

![硬币识别3](/images/type11.png)

教狗坐下(反向激励) - 增强学习

![教狗坐下1](/images/type12.png)

教狗坐下(正向激励) - 增强学习

![教狗坐下2](/images/type13.png)

总结
- 监督式学习：拿到的训练样本 D 既有输入特征 x，也有输出标签 y
- 非监督式学习：拿到的训练样本 D 没有输出标签 y 
- 半监督式学习：拿到的训练样本 D 一部分数据有输出标签 y ，而另一部分数据没有输出标签 y
- 增强学习：给模型一些输入，如果反馈结果良好，就给其正向激励，如果反馈结果不好，就给其反向激励

![总结2](/images/type14.png)

## Learning with Different Protocol f 基于协议(映射)

还是硬币识别问题 - Batch Learning

![硬币识别问题](/images/type15.png)

更多 Batch Learning

![Batch](/images/type16.png)

Online Learning

![Online](/images/type17.png)

Active Learning

![Active](/images/type18.png)

总结
- Batch Learning 一次性拿到整个 D
- Online Learning 根据数据一个个进来，同步更新我们的算法
- Active Learning 让机器具备主动问问题的能力

![总结3](/images/type19.png)

## Learning with Different Input Space X 基于输入空间
再次回到信用贷款审核问题(输入特征都属于实数域)- 具体特征

![审核](/images/type20.png)

更多的具体特征

![更多的具体特征](/images/type21.png)

手写数字识别问题 - 原始特征

![原始特征](/images/type22.png)

手写数字识别问题 - 原始特征转化为具体特征

![原始特征转化为具体特征](/images/type23.png)

评级预测问题 - 抽象特征

![抽象特征](/images/type24.png)

总结
- concrete features 具体特征
- raw features 原始特征
- abstract features 抽象特征

将一些抽象的特征转换为具体的特征，是机器学习过程中非常重要的一个环节

![总结4](/images/type25.png)

## 下一课

[Feasibility of Learning](/note/MLF/mlf04.md)