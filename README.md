第一步：安装JDK
第二步：安装Scala
1) http://www.scala-lang.org/download/ 	下载2.11
2) 增加PATH 变量，比如解压目录是C:\Program Files (x86)\scala，然后将“C:\Program Files (x86)\scala\bin;”加到环境变量path中
3) 进入cmd 界面测试Scala 是否安装成功:  C:\Users\admin>scala

第三步： 安装Spark，配置Spark环境变量
1）下载Spark 下载地址：http://spark.apache.org/downloads.html   下载版本： spark-2.3.0-bin-hadoop2.6
2） 增加环境变量
新增SPARK_HOME 变量，值：C:\Apache Spark\spark-1.6.2-bin-hadoop2.6
新增SPARK_CLASSPATH 变量，值：;C:\Apache Spark\spark-1.6.2-bin-hadoop2.6\jars;
增加PATH变量，补充：;C:\Apache Spark\spark-1.6.2-bin-hadoop2.6\bin

第四步：安装Hadoop工具包
       Spark是基于Hadoop之上的，运行过程中会调用相关Hadoop库，如果没配置相关Hadoop运行环境，会提示相关出错信息，虽然也不影响运行。Windows下开发Spark不需要在本地安装Hadoop，但是需要winutils.exe、hadoop.dll等文件。
1）下载Windows下Hadoop工具包
下载地址：https://github.com/sdravida/hadoop2.6_Win_x64/tree/master/bin
https://www.barik.net/archive/2015/01/19/172716/
2） 增加环境变量
系统Path变量中：D:\hadoop-2.6.0\bin；同时新建HADOOP_HOME变量，变量值为：D:\hadoop-2.6.0

第四步：配置开发工具
IDEA:
1 安装scala插件
2 新建Scala项目，参考项目先Github
3 配置项目
              1)Scale版本
              2) 引入外部库，使用用Maven或非Maven导入D:\Programs\spark-2.3.0-bin-hadoop2.6\jars 全部Jar导
              3）运行Run/Debug时，Edit Configuration设置
              4）生成Jar包时配置，之后使用Build / Build Aritfacts生成Jar包

第五步：本地模式运行
D:\Programs\spark-2.3.0-bin-hadoop2.6\bin\spark-submit --master local --class com.divino.SimpleApp ScaleSparkTest2.jar




