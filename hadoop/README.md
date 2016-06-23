# 镜像

index.csphere.cn/csphere/hadoop-cluster:latest

也可以换成 docker hub 的镜像:  kiwenlau/hadoop:1.0

# 使用

部署完成之后，访问 hadoop-master 的 :50070 端口，可以看到控制面板


# 增加 hadoop-slave 节点

`hadoop-master` 服务只能有一个容器，`hadoop-slave` 服务可以有多个容器

为 `hadoop-slave` 增加容器之后，需要重新发布 `hadoop-master` 的 `slaves` 配置文件，才能生效

# 测试

进入 `hadoop-master` 服务的终端，执行 `./run-wordcount.sh`

