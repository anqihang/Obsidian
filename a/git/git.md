工作区(workspace)--暂存区(staging area)--版本库(local repositiory)--远程仓库(remote repository)
master：默认主分支
origin：默认远程版本库
Head：默认开发分支
Head^：Head的父提交 
\# 配置

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
\# 
	

```
#
	git config --list ---配置信息
# 创建仓库
	git  init [dir] ---初始化一个本地库
	git clone [url] ---拷贝一份远程仓库到本地库
# 提交和修改
	git add [file/dir/.]    ---将工作区的文件提交到暂存区（跟踪文件）
	git commit -m "[descript message]" ---提交暂存区文件到版本库
	git commit --amend  ---重新提交
    #-------------------#
	git status [-s简洁]---查看仓库的状态，显示变更的文件
	git diff   ---比较暂存区和工作区的差异
	git reset [--hard/soft/mixed] ---版本回退
	git rm     ---将文件从暂存区或 工作区删除
	git mv     ---移动或重命名工作区文件
# 分支
	git branch [branch-name]   ---创建分支
	git checkout [branch-name] ---切换分支
	git merge [branch-name]    ---合并分支
	git branch -d [branch-name]---删除分支
	git rebase [master]        ---变基
# 日志
	git log   ---查看历史提交记录
	git blame ---列出指定文件的历史修改记录
# 远程操作
	git remote ---添加远程库的简洁变量origin
	git fetch  --- 从远程库获取项目到本地库(版本库)[增量拉取]
	git pull   ---从远程库拉取项目到工作区
	git push [branch] ---从版本库推送项目到远程库
#标签(lightweght)轻量标签(annotated)附注标签
	git tag
	
	
```