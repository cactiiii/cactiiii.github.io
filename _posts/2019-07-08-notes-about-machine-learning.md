---
layout: my_post
categories: [offer]
---

[QUORA官方的Data Science页面](https://www.quora.com/topic/Data-Science)

### 必备技能

微积分

线性代数

python

**LinkedIn**

要会讲故事

### 学习

[Harvard的CS109](http://cs109.github.io/2015/)

[Kaggle](https://www.kaggle.com/competitions)

[特征工程](https://www.quora.com/What-are-some-best-practices-in-Feature-Engineering)

[特征工程](https://nbviewer.jupyter.org/github/aguschin/kaggle/blob/master/forestCoverType_featuresEngineering.ipynb)

[凸优化](http://stanford.edu/~boyd/cvxbook/)

[NLP](https://www.quora.com/How-do-I-learn-Natural-Language-Processing-NLP)

使用模型vc维信息确定需要的训练数据大小？

解决训练数据不平衡问题：过采样、欠采样、集成学习。
* [知乎链接](https://www.zhihu.com/question/269698662)中提到一个结论：使用过采样（或SMOTE）+强正则模型（如XGBoost）可能比较适合不平衡的数据。拿到一个新的数据时，可以不妨直接先试试这个方法，作为基准（Baseline）

batch normalisation? It can help reduce the amount of data required.

rnn 使用正交初始化解决梯度消失/爆炸问题

神经网络使用dropout缓解过拟合

gnn(图神经网络）是什么东西？

训练复杂模型时使用权重衰减（L2正则）有助于稳定训练流程

auto-encoder是什么？

在参加比赛的时候，还可以利用test data作文章， 进行无监督训练或者pseudo-labeling

[batch normalization](https://arxiv.org/abs/1502.03167)

推荐算法主要可以分为基于内容的、协同过滤的、基于知识的

强化学习？

AutoML?

阿里DIN?

CBOW 从源上下文字词（“the cat sits on the”）中预测目标字词（例如“mat”），而 skip-gram 则逆向而行，从目标字词中预测源上下文字词。这种调换似乎是一种随意的选择，但从统计学上来看，它有助于 CBOW 整理很多分布信息（通过将整个上下文视为一个观察对象）。在大多数情况下，这对于小型数据集来说是很有用的。但是，skip-gram 将每个上下文-目标对视为一个新的观察对象，当我们使用大型数据集时，skip-gram 似乎能发挥更好的效果。
