# Deploy Mesos with cSphere
### 注意事项
镜像中的docker client是v1.11.2，而cSphere的docker是1.9.1,
直接使用镜像中的docker无法与宿主机上的docker daemon进行通信，
所以需要找个1.9.1的静态链接的docker二进制程序映射到容器的/usr/bin/docker

本模板中假定1.9.1的静态Docker二进制放在了`/root/docker`

docker 1.9.1可以从这里下载： https://raw.githubusercontent.com/wiki/nicescale/docker-machine/docker.bz2
