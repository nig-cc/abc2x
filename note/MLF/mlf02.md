# Learning to Answer Yes/No 分辨是非
## Perceptron Hypothesis Set 感知器假设集
### 信用贷款模型

![信用贷款模型](/images/xydk.png)

h(x) 的表达式做如下变换：

![h(x)简化](/images/hxjh.png)

h(x) 二维可视化：

![h(x)二维可视化](/images/hx2d.png)

## Perceptron Learning Algorithm 感知器学习算法

- 目标 -> 从 h(x) 找到 g，使得 g ≈ f(未知)
- 思想 -> 随意取一条线，然后根据错误点进行修正，直到所有的点都完全分类正确

![PLA 模型](/images/plamx.png)

图解 PLA 修正过程：

![修正01](/images/xz01.png) ![修正02](/images/xz02.png) ![修正03](/images/xz03.png)
![修正04](/images/xz04.png) ![修正05](/images/xz05.png) ![修正06](/images/xz06.png)
![修正07](/images/xz07.png) ![修正08](/images/xz08.png) ![修正09](/images/xz09.png)
![修正10](/images/xz10.png) ![修正11](/images/xz11.png) 

## Guarantee of PLA

PLA 的终止条件，就是 D 是线性可分。这样对于任意点存在

![完全分开](/images/gpla01.png)

内积越大表示越接近

![内积](/images/gpla02.png)

向量长度相差不大
	
![大小](/images/gpla03.png)

因此

![结论](/images/gpla04.jpg)

也就是说，迭代次数 T 是有上界的

![定义](/images/gpla06.jpg)

![迭代次数](/images/gpla05.png)

## Non-Separable Data



