# DataHref
mllib、scikit等数据挖掘工具的教程

官方网站：[http://datahref.com/](http://datahref.com/)


点击进入mllib、scikit等目录可以查看不同工具的教程，教程不断更新中...

教程列表：

###MLlib

+ [MLlib的kmeans算法](https://github.com/CrawlScript/DataHref/blob/master/mllib/kmeans.md)

###scikit

+ [scikit的svm接口](https://github.com/CrawlScript/DataHref/blob/master/scikit/svm.md)
+ [scikit中的决策树](https://github.com/CrawlScript/DataHref/blob/master/scikit/decision_tree.md)

###libsvm

+ [libsvm编译方法](https://github.com/CrawlScript/DataHref/blob/master/libsvm/compile.md)

###算法

+ [数据挖掘十大算法](https://github.com/CrawlScript/DataHref/blob/master/algorithm/top10.md)


###开源数据挖掘工具简介



####MLlib

MLlib是spark上的机器学习库，具有方便使用的用户接口，适合在大数据上进行数据挖掘。虽然MLlib被设计在spark集群上运行，用户仍可以在单机环境，甚至是windows下使用，且不需要配置spark环境，非常方便科研使用。


####Mahout

Mahout时hadoop上的机器学习库，封装了很多常用算法，如kmeans、lda，也可以处理大数据，但hadoop上的东西用起来毕竟不是特别方便。Mahout相对来说比较适合做工程，不大适合科研人员使用。



####scikit


对于有python基础的人来说，scikit是一个非常好的选择，scikit封装了很多机器学习方法，用户接口也非常简洁，例如可以用3行代码完成一个svm的训练，或一个决策树的训练。scikit配合相关的图形库可以很好地进行数据可视化，这对数据挖掘是非常有帮助的。scikit可以用内存作为输入输出，非常方便调试，适合开发及科研。


####Weka

Weka是一个老牌的数据挖掘软件，封装了大量的数据挖掘算法，并且提供了一个界面来执行各种算法，界面也包含了一定的可视化功能。但实在是太难用，且缺乏文档，既不适合工程用，也不适合科研用，不过可以当做玩具，来简单了解各种挖掘算法。

####RapidMinner


RapidMiner为数据挖掘提供了一个非常友好的界面，用户拖拖鼠标即可创建一个数据挖局的工作流，软件不仅封装了许多常用的数据挖掘算法，并且提供了各种数据输入输出的方式，方便数据分析和科研使用：

![](https://rapidminer.com/wp-content/uploads/2013/11/drag1.png)







