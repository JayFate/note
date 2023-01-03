解决国内安装 npm 包失败的问题

```bash
# 方法1，先安装 cnpm, 然后使用 cnpm 安装
sudo npm install -g cnpm --registry=https://registry.npm.taobao.org

# 方法2，安装 nrm，使用 nrm 将 npm 仓库设为淘宝仓库
sudo npm install -g nrm --registry=https://registry.npm.taobao.org
nrm ls
nrm use taobao
```

使用淘宝仓库安装

```bash
 npm i --registry=https://registry.npm.taobao.org/
 ```

### 2.1 配置国内镜像源

npm和yarn默认是从国外源站拉取依赖包的，为提高下载速度和稳定性，建议配置为国内镜像源。

yarn registry国内镜像：

```bash
yarn config set registry https://registry.npmmirror.com
```

npm registry国内镜像：

```bash
npm config set registry https://registry.npmmirror.com
```

yarn node-sass国内镜像：

```bash
yarn config set SASS_BINARY_SITE https://npmmirror.com/mirrors/node-sass/
```

npm node-sass国内镜像：

```bash
npm config set SASS_BINARY_SITE https://npmmirror.com/mirrors/node-sass/
```

如果不清楚本地当前yarn或者npm的配置，可以执行以下命令查看：

yarn查看方法：

```bash
yarn config list
```

npm查看方法：

```bash
npm config list
```

