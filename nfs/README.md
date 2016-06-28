## nfs server使用

```bash
docker run -d --privileged -v /:/hostroot:ro microimages/nfs-server  /exports/dir1 /exports/dir2 /exports/dir3 ...
```

注意：

- 特权模式
- 映射根文件系统方便载入nfsd内核模块
- 导出的目录一律放到/exports前缀目录下

## nfs client使用

```bash
docker run -d --privileged microimages/nfs-client
```
