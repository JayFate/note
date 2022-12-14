解决国内安装 npm 包失败的问题

```bash
# 方法1，先安装 cnpm, 然后使用 cnpm 安装
sudo npm install -g cnpm --registry=https://registry.npm.taobao.org

# 方法2，安装 nrm，使用 nrm 将 npm 仓库设为淘宝仓库
sudo npm install -g nrm --registry=https://registry.npm.taobao.org
nrm ls
nrm use taobao
```
