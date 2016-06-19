# oracle 11G
该软件为商业软件，请自行购买oracle授权

## oracle11G数据库运行
该镜像在运行时，打开了特权模式，并且在容器内部重新挂载了/dev/shm，默认大小为主机内存的1/4

## 存储
默认映射了/data/db到容器的/u01/app/oradata目录

## 管理界面
使用X11Forward特性，由于oracle容器中的sshd配置中已经开启了X11Forward:
```
X11Forwarding yes
```

登录到oracle容器中:

```
ssh -X oracle@your-oracle-ip

[oracle@oraclehost: ~]$ dbca
```

将会打开oracle的配置助手面板，可以按照向导一步步创建你的数据库了

如果有遇到 `DISPLAY not set` 的错误，往往是您的桌面不支持X。具体如何在不同的操作系统下面配置X11Fording，请查看具体文档。
