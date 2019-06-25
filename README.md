# spark-docker
以docker的方式安装spark集群

# 使用
下载spark和hadoop包并放入pkg目录
```
hadoop-3.1.2.tar.gz  
spark-2.4.3-bin-hadoop2.7.tgz
```

注意上面的包名对应3个Dockerfile里面的ENV，如果版本有变化，需要对应修改
```
ENV SPARK_VERSION=spark-2.4.3-bin-hadoop2.7
ENV HADOOP_VERSION=hadoop-3.1.2
```

安装base
```
$ docker build -t spark-base -f Dockerfile-spark-base .
```

安装master和worker
```
$ docker build -t spark-master -f Dockerfile-spark-master .
$ docker build -t spark-worker -f Dockerfile-spark-worker .
```

启动
```
$ docker-compose up
```

# 访问测试
请求地址根据docker-compose.yml的配置，默认为 http://IP:8001 .
