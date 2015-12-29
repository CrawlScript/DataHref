###libsvm编译方法

libsvm提供了多语言版本，本文介绍C++版和java版的编译。

首先进入libsvm的Github首页下载源码，地址：[https://github.com/cjlin1/libsvm](https://github.com/cjlin1/libsvm)。进入首页后点击右侧DownloadZip下载解压，或直接使用git clone复制项目。


####编译C++版libsvm

例如我们要编译svm的训练，进入libsvm根目录，执行命令：

    g++ svm.cpp svm.h svm-train.c -o svm_train

可以编译得到svm_train，用命令./svm_train就可以执行svm训练功能。


####编译JAVA版libsvm

进入libsvm/java目录，将其中的libsvm目录和多个java文件复制到JAVA项目的源码根目录即可。



