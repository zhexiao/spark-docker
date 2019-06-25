# spark-docker
以docker的方式安装spark集群

# 安装镜像
安装base
```
$ docker build -t spark-base -f Dockerfile-spark-base .
```

安装master和worker
```
$ docker build -t spark-master -f Dockerfile-spark-master .
$ docker build -t spark-worker -f Dockerfile-spark-worker .
```
