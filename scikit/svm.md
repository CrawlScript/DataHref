###scikit的svm接口

scikit是一个非常好用的机器学习库，基于python。

首先需要安装scikit，建议在linux下使用，官方安装教程：[http://scikit-learn.org/stable/install.html](http://scikit-learn.org/stable/install.html)

scikit的svm接口非常简单：

    from sklearn import svm
    X = [[0, 0], [1, 1]]
    y = [0, 1]
    clf = svm.SVC()
    clf.fit(X, y)  
    clf.predict([[2., 2.]])

x是训练数据集，包含两个样本，[0,0]和[1,1]，每个样本都是二维数据。每个样本的label(即类别)保存在y中，第一个样本类别为0，第二个样本类别为2。

通过svm.SVC()初始化一个SVM分类器，通过fit()方法训练分类器，最终，使用predict()方法来预测新样本的类别。
