---
layout: my_post
categories: [paper translate]
---
## 摘要
已经有数种协同过滤的方法被研究，但是很少有针对大型（数百万用户和物品）和动态（底层物品集合不断变化）背景的研究报告。本文中我们描述了为谷歌新闻用户生成个性化推荐的协同过滤方法。我们使用三种方法生成推荐：使用MinHash聚类的协同过滤，PLSI（Probabilistic Latent Semantic Indexing），和共同访问计数。我们使用线性模型结合不同算法的推荐。我们的方法对内容透明，因此独立于领域，使得它可以轻松适用于其他应用和语言。本文将详细描述我们的算法和系统设置，并且报告在谷歌新闻运行推荐引擎的结果。

## 介绍
互联网并不缺少内容。挑战在于为你自己找到合适的内容：能满足你当前信息需求的或者你可能喜欢读的。搜索引擎有助于解决第一个问题；尤其是如果你在在寻找可以被表述为关键字查询的特定内容。然而在很多情况下，用户可能甚至不知道要找什么。通常新闻、电影都是如此，用户最终反而浏览像news.google.com，www.netflix.com这些网站。带着一种“给我些有趣的东西看”的态度寻找一些可能令他们感兴趣的东西。在这种情况下，我们希望根据用户在相关网站上的历史行为所展示的兴趣为她展示推荐。

协同过滤是一种旨在基于用户和社区数据学习用户偏好并且进行推荐的技术。它是对基于内容过滤（如基于关键词的搜索）的补充基础。协同过滤最广为人知的应用可能是亚马逊网站，它利用用户过去的购物历史来推荐新产品。研究界在过去已经提出了各种协同过滤方法（详见第3节）。我们的目标是建立一个可伸缩的在线推荐引擎，可以在诸如谷歌新闻的大型网站上进行个性化推荐。尽管对推荐质量有要求，但下面这些要求使我们有别于大部分已知的推荐系统。
**可伸缩性**：谷歌新闻在几天时间内就有数百万唯一用户访问。物品（即由新闻文章聚类标识的新闻故事）的数量也是数百万。
**物品变动**：大多数系统假设底层的物品集是静态或者变动很小，因而通过近似更新模型或频繁重建模型来合并新物品。通常情况下重建是昂贵的任务，不会太频繁（每几小时）地完成。但是，对于谷歌新闻这样的机构，底层的物品集合每几分钟就会变动（插入和删除），并且在任何时候，感兴趣的故事都是最近几小时内出现过的。因此，任何超过几小时的模型可能不再有吸引力，并且部分更新也将不起作用。
基于上述原因，我们发现现有的推荐系统不符合我们的需求，开始着手于新型可伸缩算法的新方法。我们相信亚马逊也在相似的规模上进行推荐。然而，我们与他们系统的显著不同在于第二点（物品变动）。本文介绍了我们的方法和基本算法，以及相关的系统组件。本文剩余部分组织如下：第2节描述了问题设定。第3节对相关工作作了简要总结。第4节介绍了我们的算法；即使用Minhash和PLSI的用户聚类，以及基于物品-物品共同访问的推荐。第5节描述如何实现这样的系统。第6节报告了与其他协同过滤算法对比分析的结果以及在实时流量上的质量评估。在第7节我们以一些结论和开放问题结束本文。

## 问题设置
谷歌新闻是一个计算机生成的新闻网站，汇集了全球4500多家新闻源的新闻文章，将类似的故事分组，并根据每个用户的个性化兴趣展示出来。有各种国家和语言的版本。谷歌新闻的主页面在左上角展示热点新闻，然后是分类栏目，如世界、美国、商业等。每个栏目包括该分类下的前3个头条。在热点新闻的左边是一个导航栏，把每个分类链接到一个包含该分类所有故事的页面。这是未登录用户的主页面格式。另外，如果你用谷歌账号登录并且打开由各种谷歌产品网站提供的“搜索历史”功能，你将享受两个额外的特色：

（a）谷歌将记录你对新闻故事的搜索查询和点击，并使你可以在线访问它们。这让你可以轻松浏览过去读过的文章。

（b）就在热点新闻的下方，你会看到一个名为“为你推荐”的栏目，以及三条根据你的过去点击历史推荐的三个故事。

我们项目的目标是


试着插入公式\\(\sum_{i=0}^Ni^2\\)
$$\alpha=\frac{\beta}{\theta}$$
哈哈5
When \\(a \ne 0\\), there are two solutions to \\(ax^2 + bx + c = 0\\) and they are
  $$x = {-b \pm \sqrt{b^2-4ac} \over 2a}.$$
  
$$theta_k = (C_k + \alpha) / (\sum_k C_k + K\alpha)$$
