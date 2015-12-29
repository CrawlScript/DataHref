###数据挖掘十大算法

本帖收集数据挖掘十大算法相关资料，持续更新中。

本文部分信息引自PPT：[Top10DMAlgorithms](http://www.cs.uvm.edu/~xwu/PPT/Top10DMAlgorithms-C.pdf)

数据挖掘十大算法：

####C4.5, presented by Hiroshi Motoda

C4.5决策树

C4.5算法是由Ross Quinlan开发的用于产生决策树的算法。该算法是对Ross Quinlan之前开发的ID3算法的一个扩展。C4.5算法产生的决策树可以被用作分类目的，因此该算法也可以用于统计分类。


####K-Means, presented by Joydeep Ghosh

KMeans聚类

k-平均算法源于信号处理中的一种矢量量化方法，现在则更多地作为一种聚类分析方法流行于数据挖掘领域。k-平均聚类的目的是：把n个点（可以是样本的一次观察或一个实例）划分到k个聚类中，使得每个点都属于离他最近的均值（此即聚类中心）对应的聚类，以之作为聚类的标准。这个问题将归结为一个把数据空间划分为Voronoi cells的问题。

资料：

[KMeans++源码（JAVA）](http://datahref.com/book/article.php?article=mining_kmeans_source)


####SVM, presented by Qiang Yang

支持向量机

支持向量机是一种监督式学习的方法，可广泛地应用于统计分类以及回归分析。支持向量机属于一般化线性分类器，也可以被认为是提克洛夫规范化（Tikhonov Regularization）方法的一个特例。这族分类器的特点是他们能够同时最小化经验误差与最大化几何边缘区，因此支持向量机也被称为最大边缘区分类器。

资料：

[libsvm的Github主页](https://github.com/cjlin1/libsvm)

[scikit的svm接口（PYTHON）](http://datahref.com/book/article.php?article=mining_scikit_svm)

[svmjs——js上的svm库](http://datahref.com/book/article.php?article=mining_svmjs)


####Apriori, presented by Christos Faloutsos

Apriori关联规则


先验算法是关联式规则中的经典算法之一。在关联式规则中，一般对于给定的项目集合（例如，零售交易集合，每个集合都列出的单个商品的购买信息），算法通常尝试在项目集合中找出至少有C个相同的子集。先验算法采用自底向上的处理方法，即频繁子集每次只扩展一个对象（该步骤被称为候选集产生），并且候选集由数据进行检验。当不再产生符合条件的扩展对象时，算法终止。

####EM, presented by Joydeep Ghosh
期望最大化算法

最大期望算法在统计中被用于寻找，依赖于不可观察的隐性变量的概率模型中，参数的最大似然估计。在统计计算中，最大期望算法是在概率模型中寻找参数最大似然估计或者最大后验估计的算法，其中概率模型依赖于无法观测的隐藏变量（Latent Variable）。最大期望经常用在机器学习和计算机视觉的数据聚类（Data Clustering）领域。最大期望算法经过两个步骤交替进行计算，第一步是计算期望（E），利用对隐藏变量的现有估计值，计算其最大似然估计值；第二步是最大化（M），最大化在E步上求得的最大似然值来计算参数的值。M步上找到的参数估计值被用于下一个E步计算中，这个过程不断交替进行。

####PageRank, presented by Christos Faloutsos

PageRank排序算法

PageRank通过网络浩瀚的超链接关系来确定一个页面的等级。Google把从A页面到B页面的链接解释为A页面给B页面投票，Google根据投票来源（甚至来源的来源，即链接到A页面的页面）和投票目标的等级来决定新的等级。简单的说，一个高等级的页面可以使其他低等级页面的等级提升。

####AdaBoost, presented by Zhi-Hua Zhou

AdaBoost分类

AdaBoost，是英文"Adaptive Boosting"（自适应增强）的缩写，是一种机器学习方法，由Yoav Freund和Robert Schapire提出。AdaBoost方法的自适应在于：前一个分类器分错的样本会被用来训练下一个分类器。AdaBoost方法对于噪声数据和异常数据很敏感。但在一些问题中，AdaBoost方法相对于大多数其它学习算法而言，不会很容易出现过拟合现象。AdaBoost方法中使用的分类器可能很弱（比如出现很大错误率），但只要它的分类效果比随机好一点（比如两类问题分类错误率略小于0.5），就能够改善最终得到的模型。而错误率高于随机分类器的弱分类器也是有用的，因为在最终得到的多个分类器的线性组合中，可以给它们赋予负系数，同样也能提升分类效果。


####kNN, presented by Vipin Kumar

k-邻近分类

K-NN是一种基于实例的学习，或者是局部近似和将所有计算推迟到分类之后的惰性学习。k-近邻算法是所有的机器学习算法中最简单的之一。


####Naive Bayes, presented by Qiang Yang

朴素贝叶斯

在机器学习中，朴素贝叶斯分类器是一系列以假设特征之间强（朴素）独立下运用贝叶斯定理为基础的简单概率分类器。

####CART, presented by Dan Steinberg

CART决策树
