# 机器学习-54:集成学习分类算法(ada-boost)(含python源码)

> [机器学习原理与实践(开源图书)-总目录](https://blog.csdn.net/shareviews/article/details/83030331)

集成学习(ada-boost)分类算法属于监督学习算法。常用分类算法包括：逻辑回归(Logistic Regression, LR)、K最近邻(k-Nearest Neighbor, KNN)、朴素贝叶斯模型(Naive Bayesian Model, NBM)、隐马尔科夫模型(Hidden Markov Model)、支持向量机(Support Vector Machine)、决策树(Decision Tree)、神经网络(Neural Network)和集成学习(ada-boost)。

> 告别碎片阅读，构成知识谱系。一起阅读和完善: [机器学习原理与实践(开源图书)](https://github.com/media-tm/MTOpenML)

在实际部署场合，由于数据的多样性和复杂性，前期评估的分类模型往往不是最佳的。对此通过多种分类方法的融合即集成学习有利于可以这个缺陷，增强了分类算法的鲁棒性。集成学习(ada-boost)是一种机器学习范式，它试图通过连续调用单个的学习算法，获得不同的基学习器，然后根据规则组合这些学习器来解决同一个问题，可以显著的提高学习系统的泛化能力。

## 1 算法原理

集成学习(ada-boost)分类算法是通过组合多个基分类器(base classifier)来完成学习任务。基分类器一般采用的是弱可学习(weakly learnable)分类器，通过集成学习，组合成一个强可学习(strongly learnable)分类器。所谓弱可学习，是指学习的正确率仅略优于随机猜测的多项式学习算法；强可学习指正确率较高的多项式学习算法。集成学习的泛化能力优于单一的基分类器，融合后的分类结果准确率更高。

集成学习(ada-boost)分类算法采用加法模型，使用若干个弱分类器以加权平均的形式构成强分类器。集成学习利用前向分步学习策略，利用前一个弱学习器的结果来更新后一个弱学习器的训练集权重。集成学习的损失函数一般采用指数函数。

集成学习(ada-boost)分类算法的核心步骤如下:

- 数据清洗：数据规范化, 了解数据的基本特征;
- 从训练集用初始权重训练出若干个弱学习器;
- 根据弱学习的学习误差率表现来更新训练样本的权重;
- 使用训练集继续训练调整权重后的弱学习器;
- 反复迭代，直到弱学习器的数量降到预定值X;
- 将X个弱学习器通过集合策略进行融合得到强学习器。

集成学习(ada-boost)分类算法的核心优势如下：

- 计算伸缩性: 计算复杂度可控;
- 参数依赖性: 可调节参数较少;
- 普适性能力: 不用特征筛选，不用担心过拟合问题；
- 抗噪音能力: 对异常样本敏感，最终影响强学习器的预测准确性;
- 结果解释性: Adaboost算法是一个框架，构建弱学习器方法灵活。

## 2 算法实例

[TODO, Coming Soon!]

## 3 典型应用

- [深度学习原理与实践(开源图书)-总目录](https://blog.csdn.net/shareviews/article/details/83040730)
- [机器学习原理与实践(开源图书)-总目录](https://blog.csdn.net/shareviews/article/details/83030331)
- [Github: 机器学习&深度学习理论与实践(开源图书)](https://github.com/media-tm/MTOpenML)

## 参考资料

- [1] 周志华. 机器学习. 清华大学出版社. 2016.
- [2] [日]杉山将. 图解机器学习. 人民邮电出版社. 2015.
- [3] 佩德罗·多明戈斯. 终极算法-机器学习和人工智能如何重塑世界. 中信出版社. 2018.
- [4] 李航. 统计学习方法. 2012.