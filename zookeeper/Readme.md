镜像：mesoscloud/zookeeper

docker pull mesoscloud/zookeeper 

push到本地registry

导入的时候选择包含mesoscloud/zookeeper的registry

查看zookeeper集群状态:

```bash
$ zkServer.sh  status
JMX enabled by default
Using config: /opt/zookeeper/bin/../conf/zoo.cfg
Mode: leader
```

```bash
$ echo stat | curl -s  telnet://localhost:2181
Zookeeper version: 3.4.6-1569965, built on 02/20/2014 09:09 GMT
Clients:
 /0:0:0:0:0:0:0:1:46186[0](queued=0,recved=1,sent=0)

Latency min/avg/max: 0/0/0
Received: 2
Sent: 1
Connections: 1
Outstanding: 0
Zxid: 0x100000000
Mode: leader
Node count: 4
```

