## docker 新手练习

https://www.jianshu.com/p/bd5a8945e071

```bash
docker run -d -p 81:80 nginx
# 81 是宿主本机端口
# -d 以后台守护进程启动

docker build -t zcdf .
# -t tag
# . 镜像构建上下文  https://yeasy.gitbook.io/docker_practice/image/build#qi-ta-docker-build-de-yong-fa
```

