## 一、入门文档

1. [Docker 入门教程-阮一峰](https://www.ruanyifeng.com/blog/2018/02/docker-tutorial.html)
2. [docker入门到实践](https://yeasy.gitbook.io/docker_practice/network/linking)

## docker 新手练习

https://www.jianshu.com/p/bd5a8945e071

```bash
docker run -d -p 81:80 nginx
# 81 是宿主本机端口
# -d 以后台守护进程启动

docker run -d -p 92:80 --name container-name -v `pwd`:/usr/share/nginx/html nginx
# --name 指定运行起来的容器名
# nginx 运行使用的镜像名
# -v:外部路径：内部路径，可以进行文件的映射，可以进行数据的保存，将数据保存在外部存储盘中

docker run -it --rm ubuntu:18.04 bash
# -it：以交互式终端方式运行，一个是 -i：交互式操作，一个是 -t 终端。我们这里打算进入 bash 执行一些命令并查看返回结果，因此我们需要交互式终端。
# --rm：这个参数是说容器退出后随之将其删除。默认情况下，为了排障需求，退出的容器并不会立即删除，除非手动 docker rm。我们这里只是随便执行个命令，看看结果，不需要排障和保留结果，因此使用 --rm 可以避免浪费空间。

docker build -t zcdf .
# -t tag
# . 镜像构建上下文  https://yeasy.gitbook.io/docker_practice/image/build#qi-ta-docker-build-de-yong-fa

docker image ls
# 列出已经下载下来的镜像，只会显示顶层镜像

docker image ls -a
# 显示包括中间层镜像在内的所有镜像

docker image ls ubuntu
# 根据仓库名列出镜像
docker image ls ubuntu:18.04
# 列出特定的某个镜像，也就是说指定仓库名和标签

docker image ls -f since=mongo:3.2
# 列出 在 mongo:3.2 之后建立的镜像

docker image prune
# 删除 虚悬镜像

docker image rm 501ad78535f0
# 删除镜像，实际上是删除镜像标签。
# 当该镜像所有的标签都被取消了，该镜像很可能会失去了存在的意义，因此会触发删除行为。
docker image rm centos

docker image rm $(docker image ls -q redis)
# 删除所有仓库名为 redis 的镜像

docker image rm $(docker image ls -q -f before=mongo:3.2)
# 删除所有在 mongo:3.2 之前的镜像

```






