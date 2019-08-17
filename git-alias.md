# alias
## 我们知道执行一些Git命令其实操作很频繁比如
```
git commit
git checkout
git branch
git status
```
## 你可将上面的进行alias配置
```
git config --global alias.co checkout #别名
git config --global alias.c commit
git config --global alias.br branch
git config --global alias.s status
```
## 还可以设置组合
```
git config --global alias.psm 'push origin master'
git config --global alias.plm 'pull origin master'
```
## 详细日志文件
```
git config --global alias.lg 'log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit --date=relative'
```
## 其他配置
### git默认的编辑器是vi，如果不喜欢可以用其他编辑器，比如vim
```
git config --global core.editor 'vim' #设置Editor使用vim
```
### 不喜欢自己终端的颜色，你可以输入一下命令改色
```
git config --global color.ui true
```
### 其他的一些配置
```
git config --global core.quotepath false # 设置显示中文文件名
```
**上面的配置都在`~/.gitconfig`文件下的，你可以找到这个文件查看自己的配置，也可以输入`git config -l`命令查看**
