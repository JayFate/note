查看全局配置文件的位置

```bash
git config --list --show-origin --show-scope
# /home/computer-username/.gitconfig
```

配置全局用户名和邮箱

```bash
git config --global user.name "pengjie"
git config --global user.email "37610029@qq.com"
```

生成公钥和私钥

```bash
ssh-keygen -t rsa -C "37610029@qq.com"
```

然后连续按三次回车键。生成的公钥和私钥的位置分别是：

```bash
~/.ssh/id_rsa.pub
~/.ssh/id_rsa
```

然后 `cat ~/.ssh/id_rsa.pub` 将公钥配置到 github / gitlab 中。
