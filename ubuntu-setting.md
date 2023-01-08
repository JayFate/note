## set keyboard mapping

Updated for 18.04 since none of the provided answers seemed to work on my system. 
I did a clean install of 18.04 and attempting to use a wired aluminum apple keyboard. 
Default behavior of Left Super on English US is mapped to Gnome Desktop Dashboard. 
Tweak tool had all the necessary settings in an easy to use GUI!

```bash
sudo apt install gnome-tweak-tool
```
First I swapped the dashboard hotkey to the right side and then under "Additional Layout Options" 
you can use "Ctrl position/ Swap Left Win with Left Ctrl" to good effect.

Clear Terminal via `Ctrl+L / Ctrl+Shift+K` Shortcut

**ubuntu default shortcut**

https://stackoverflow.com/questions/9679776/how-do-i-clear-delete-the-current-line-in-terminal
http://teohm.com/blog/shortcuts-to-move-faster-in-bash-command-line/

## Ubuntu | 安装oh-my-zsh

部分插件安不上，可以单独 google 安装方法

https://www.jianshu.com/p/ba782b57ae96


### 使用 autosuggestions 插件时关闭打字机效果

```bash
code ~/.zshrc
```

在 ~/.zshrc 中加入如下代码

```bash
# 关闭打字机效果
pasteinit() {
OLD_SELF_INSERT=${${(s.:.)widgets[self-insert]}[2,3]}
 zle -N self-insert url-quote-magic
}

pastefinish() {
 zle -N self-insert $OLD_SELF_INSERT
}
 
zstyle :bracketed-paste-magic paste-init pasteinit
zstyle :bracketed-paste-magic paste-finish pastefinish
# 关闭打字机效果
```
