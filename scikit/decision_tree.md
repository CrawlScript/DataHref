###scikit中的决策树

scikit是一个非常好用的机器学习库，基于python。

首先需要安装scikit，建议在linux下使用，官方安装教程：[http://scikit-learn.org/stable/install.html](http://scikit-learn.org/stable/install.html)

scikit的决策树接口与scikit的svm接口类似，代码如下：

	from sklearn import tree
	X = [[0, 0], [1, 1]]
	Y = [0, 1]
	clf = tree.DecisionTreeClassifier()
	clf = clf.fit(X, Y)
	clf.predict([[2., 2.]])

x是训练数据集，包含两个样本，[0,0]和[1,1]，每个样本都是二维数据。每个样本的label(即类别)保存在y中，第一个样本类别为0，第二个样本类别为2。

通过tree.DecisionTreeClassifier()初始化一个决策树，通过fit()方法训练决策树，最终，使用predict()方法来预测新样本的类别。

可以将决策树保存在文件中，scikit官网有一个例子，用scikit内置的iris数据集训练决策树，最后将决策树保存在iris.dot文件中：

	from sklearn.datasets import load_iris
	from sklearn import tree
	iris = load_iris()
	clf = tree.DecisionTreeClassifier()
	clf = clf.fit(iris.data, iris.target)
	from sklearn.externals.six import StringIO
	with open("iris.dot", 'w') as f:
		f = tree.export_graphviz(clf, out_file=f)

不过打开dot文件，需要下载第三方软件。
