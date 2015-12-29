###MLlib的kmeans算法（spark）

MLlib提供了方便的kmeans接口。

要使用MLlib，在pom.xml中添加spark和mllib的依赖即可。

首先在项目中新建一个文件夹data/mllib。在data/mllib中新建一个文件kmeans_data.txt，内容如下：

    1 1
    1 2
    3 1
    4 1
    100 200
    101 201
    99 199


创建代码KMeansExample，代码如下：




    import org.apache.spark.api.java.*;
    import org.apache.spark.api.java.function.Function;
    import org.apache.spark.mllib.clustering.KMeans;
    import org.apache.spark.mllib.clustering.KMeansModel;
    import org.apache.spark.mllib.linalg.Vector;
    import org.apache.spark.mllib.linalg.Vectors;
    import org.apache.spark.SparkConf;

    public class KMeansExample {
      public static void main(String[] args) {
        SparkConf conf = new SparkConf().setAppName("K-means Example");
        JavaSparkContext sc = new JavaSparkContext(conf);

        // 从文件加载数据，数据以行加载
        // 利用rdd的map功能将行转换为向量
        String path = "data/mllib/kmeans_data.txt";
        JavaRDD<String> data = sc.textFile(path);
        JavaRDD<Vector> parsedData = data.map(
          new Function<String, Vector>() {
            //call方法会对文件的每行执行
            public Vector call(String s) {
              //向量的每个维度用空格分割
              String[] sarray = s.split(" ");
              double[] values = new double[sarray.length];
              //字符串转double
              for (int i = 0; i < sarray.length; i++)
                values[i] = Double.parseDouble(sarray[i]);
              return Vectors.dense(values);
            }
          }
        );
        parsedData.cache();

        
        int numClusters = 2;
        int numIterations = 20;
        // 执行k为2的kmeans
        KMeansModel clusters = KMeans.train(parsedData.rdd(), numClusters, numIterations);

        // 评价当前kmeans的效果，评价指标为sum of squared errors
        double WSSSE = clusters.computeCost(parsedData.rdd());
        System.out.println("Within Set Sum of Squared Errors = " + WSSSE);

        // 保存kmeans模型
        clusters.save(sc.sc(), "myModelPath");
        KMeansModel sameModel = KMeansModel.load(sc.sc(), "myModelPath");
      }
    }
