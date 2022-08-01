工作区-暂存区-版本库
master：默认主分支
origin：默认远程版本库
Head：默认开发分支
Head^：Head的父提交
#### 流程
1. **创建一个本地库[名字]**(历史版本)
```
git init [projet-name] # 新建一个目录(如果没有)用指定的名字创建一个本地仓库
git clone [url] # 下载项目和全部历史版本
``` 
3. **设置**
```
git config -e [--global] # 显示当前的git配置
项目:
git config user.name "[name(anqihang_pro)]" 
git config user.email "[email address(anqihang0106_pro@outlook.com)]"
全局:
git config --global user.name "[name()]"
git config --global user.email "[email address()]"

git config --global color.ui auto -- 启用命令行的可用着色
```
4. **添加`工作区`文件到`暂存区`**
```
git add [file]/[dir]/. # 文件/文件夹/所有
```
7. **从`暂存区`删除文件（停止追踪）**
```
git rm --cached [file]
git mv [file-original] [file-renamed] # 重命名并添加到暂存区
```
9. **将文件从`暂存区`提交到`本地库`**
```
git commit -m [file] "[descriptive message]"
git commit -amend -m "[descriptive message]" # 使用新提交代替上次的提交
```
10. ****
```

```
#### 修改
```
git status --- 列出所有需要写入的新文件或修改过的文件
git diff --- 显示尚未分档的文件差异
git add [file] --将工作区的文件添加到暂存区。对文件进行快照，进行版本管理
git diff --staged  --- 显示暂存和最后一个文件版本的差异
git reset [file] --- 解除文件缓存，但保留内容
git commit -m "[desctiptive message]" --- 从暂存区提交到本地库  将文件快照记录在历史版本中
```
#### 组变化
```
git branch --- 列出库中所有的本地分支
git branch [branch-name] --- 创建一个新的分支
git checkout [branch-name] --- 切换到指定的分支并更新工作目录
git merge [branch] --- 将指定的分支的历史记录合并到当前分支
git branch -d [branch-name] --- 删除指定分支
```
#### 重构文件名
```
git rm [file] --- 从工作目录中删除文件，并分阶段进行删除
git rm --cached [file] --- 将文件从版本控制中删除，但在本地保留文件
git mv [file-origin] [file-renamed] --- 更改文件名并准备提交

```

#### 保存片段
```
git stash --- 暂时保存所有修改过的跟踪文件
git stash pop ---列出所有储藏的变更集
git stash list --- 恢复最近存储的文件
git stash drop --- 丢弃最近存储的变更集
```
#### 历史回顾
```
git log --- 列出当前分支的历史版本
git log --follow [file] --- 列出一个文件的版本历史，包括重命名
git diff [first-branch]...[second-branch] --- 显示两个分支之间的内容差异
git show [commit] --- 输出指定提交的元数据和内容变化
```
#### 