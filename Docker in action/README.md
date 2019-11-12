## 相关资料下载
英文原版pdf [下载](http://pzpfl3y9j.bkt.clouddn.com/Docker.in.Action.pdf)

resource [下载](https://www.manning.com/downloads/1337)

## docker换源

在`/etc/docker/daemon.json`添加如下内容，切换至中科大源加速下载
```json
{
  "registry-mirrors": [
    "https://docker.mirrors.ustc.edu.cn"
  ]
}
```
