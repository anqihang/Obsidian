# 打开NeoVim
`nvim`

###### 1.1
	`h j k l`
###### 1.2不保存退出
	:q!
###### 1.3删除一个字符
	x
###### 1.4输入
	`i`
###### 1.5插入行尾
	`A`
###### 1.6打开文件
	`$ nvim file-name`
###### 2.1删除一个word
	`dw`
###### 2.2 删除到行尾
	`d$`
###### 2.3 d motion
```
w 到下一个单词开头
e 到本单词末尾
$ 到行尾
```
###### 2.4移动-数字加motion
```
2w 移动到第三个word开头
3e 移动到第三个word末尾
0  移动到行首
```
###### 2.5删除-数字加motion
```
d2w 删除两个单词
```
###### 2.6删除一行
		`2dd 删除两行`
###### 2.7撤销
```
u 撤销上一次comment 
U 让一行恢复 
ctrl-R
```
###### 3.1粘贴
	`p 粘贴删除的内容到后边 P 粘贴到前边`
###### 3.2替换
	`ra 替换成a`
###### 3.3删除单词后边的字母并写入
	`ce`
###### 3.4c加数字motion
```
c2w 删除两个word并切换为i模式
c$  删除到行尾并切换为i模式
```
###### 4.1显示文件的路径
```
C-g
G   移动到文件最后
2G  移动到2行
gg  移动到文件开头
```
###### 4.2搜索
```
/error 全局搜索error
n 查找下一个 
C-i只找一次
N 查找上一个
?error 向后搜索
C-o 回到原来的位置

```
###### 4.3显示括号
	`%`
###### 4.4匹配
```
:s/thee/the/g 全行匹配thee换成the
:#,#s/old/new/g 匹配#行到#行之间的
:%s/old/new/gc 匹配文件内所有的并询问是否改变
```
###### 5.1执行外部代码
```
:!dir 打印目录信息
```
###### 5.2保存
`:w`
###### 5.3部分保存
```
v 多选内容 :w file-name
```
###### 5.4写入检索的内容
```
:r !dir 写入目录信息
```
###### 6.1在下一行插入空行
```
o 在下一行插入空行
O 在上一行插入空行
```
###### 6.2插入
`a 和i一样只是在所选字母后边插入光标`
###### 6.3连续替换
`R r的连续版本`
###### 6.4复制
	`y motion`
###### 6.5set
###### 6.6

