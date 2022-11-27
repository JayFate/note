## docker 新手练习

https://www.jianshu.com/p/bd5a8945e071

```bash
docker run -d -p 81:80 nginx
# 81 是宿主本机端口
# -d 以后台守护进程启动

docker build -t zcdf .
# -t tag
# . 镜像构建上下文  https://yeasy.gitbook.io/docker_practice/image/build#qi-ta-docker-build-de-yong-fa

docker run -d -p 92:80 --name container-name -v `pwd`:/usr/share/nginx/html nginx
# --name 指定运行起来的容器名
# nginx 运行使用的镜像名
# -v:外部路径：内部路径，可以进行文件的映射，可以进行数据的保存，将数据保存在外部存储盘中

```

