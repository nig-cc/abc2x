# 机器学习总结 

- 基础概念：`概论` `业务理解` `数据理解` `数据准备` `模型化` `模型评估` `模型应用`
- 知名算法：`最近邻` `SVM` `线性回归` `逻辑回归` `神经网络` `梯度下降` `朴素贝叶斯` `K均值` `PCA` `决策树` `随机森林` `AdaBoost`
- 其他主题：`设计与构建` `数据不足` `流行框架`

## 概论
### 什么是机器学习

机器学习是一门帮助计算机`从已有数据中学习`并`预测未来行为、结果和趋势`的数据科学技术

![](/images/zj_jqxx.png)

### 机器学习的工作流程

工作流程：`选取数据` -> `模型化数据` -> `验证模型` -> `测试模型` -> `应用模型` -> `调试模型`

![](/images/zj_gzlc.png)

### 构建机器学习解决方案的步骤

解决方案：`提炼业务问题` -> `提取数据` -> `迭代开发模型` -> `部署模型` -> `监测性能`

模型开发：`提炼指标` -> `提取衍生特征` -> `选取特征` -> `拟合模型` -> `评估模型`

![](/images/zj_gjbz.png)

### 什么时候可以使用机器学习(以情感分析举例)

1 是否需要机器学习(`规则复杂度`和`问题规模`)

![](/images/zj_need.png)

2 能否清楚的描述问题 -> 提炼问题

- 已知`评论`，预测`情感`
    - 输入：评论文本
    - 输出：积极，消极，中立

3 是否有大量样本 -> 提取数据

- 互联网有大量数据(收集`特征`和`标签`) 

4 问题是否存在某种规律 -> 提炼规律

- 积极：很好，美好，喜欢
- 消极：不好，糟糕，没兴趣

5 能否找到更有意义的表现形式 -> 提取衍生特征

- 评论文本 -> 词向量
- 标签：积极(4-5 星)、消极(1-2 星)、中立(3 星)
- 数据图形化

6 如何评估有效 -> 提炼指标

- 准确率

![](/images/zj_when.png)

总结：有一个`复杂`任务涉及`大量`数据和`很多`变量，却`没有已知公式`时

### 模型如何创建

![](/images/zj_model.png)

### 经典学习任务

- `分类` -> 预测类别 | `回归` -> 预测数值

![](/images/zj_task.png)

## 业务理解

![](/images/zj_business.png)

### 数据科学常问的5个问题
- 是 A 还是 B？-> 分类算法
- 是怪异的？-> 不规则检测算法
- 是多少？-> 回归算法
- 如何组织？-> 聚类算法
- 现在该做啥？-> 强化学习算法

![](/images/zj_business_want.png)

## 数据理解

![](/images/zj_data.png)

### 数据近观

![](/images/zj_data_look.png)

## 数据准备

![](/images/zj_prepare.png)

![](/images/zj_process.png)