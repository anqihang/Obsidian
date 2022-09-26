`PS1='[\[\e[32m\]\u\[\e[0m\[\e[36m\]@\[\e[0m\[\e[34m\]\h\[\e[0m \[\e[1;35m\]\w\[\e[0m]\[\e[31m\]\$\[\e[0m '`

# 目录

```Markdown
bin     - Binaries(二进制文件)存放经常使用的命令
boot    - 启动Linux的核心文件，包含连接文件和镜像文件
dev     - Device(设备)存放Liunx的外部设备
etc     - Etcetera(等等)存放系统管理所需的配置文件和子目录
home    - 用户的目录
lib     - Lirary(库)存放系统最基本的动态连接共享库
lib64   -
media   - 挂载识别的设备(u盘，光驱)
mnt     - 临时挂载别的文件系统
opt     - option(可选)主机额外安装软件目录
proc    - Processes(进程)存储的是当前内核运行状态的一系列特殊文件，这个目录是一个虚拟的目录，它是系统内存的映射，我们可以通过直接访问这个目录来获取系统信息。这个目录的内容不在硬盘上而是在内存里
root    - 系统管理员的主目录
run     - 存储系统启动后的信息
sbin    - 存放系统管理员的命令
srv     - 存放服务启动后需要提取的数据
sys     - 
tmp     - temporary(临时)存放临时文件
usr     - unix shared resources(共享资源)用户的应用程序和文件，类似program files
var     - variable(变量)存放日志
```

# 文件属性


```Markdown
   0  123  456  789    username gropname size date/timelastmodify filename
[d|-][rwx][rwx][rwx] 2   root     root    4096   2019  2            bin
d#文件夹 && -#文件 && l#链接文档 && b# && c#串行端口设备
r-read可读&&w-write可写&&x-execute可执行////属主-属组-其他用户


```

- clear
- `ls`	 /list file/##查看文件
- `pwd`	 /print working directory/##打印文件路径
- `mkdir` /make directory/##创建一个新的文件夹
- `rmdir` /remove directory/##删除一个文件夹
- `rm`	 /remove/ :remove file and null directory
- `cp`	 /copy file/ :copy file to anthor file
- `mv`	 /move directory/ :move file and directory or change the name
- `cat`	 :print the content
- `shutdown` -h  now poweroff init0 halt :close the machiel
- `suhtdown` -r now reboot init6 :rebegin the machiel
- `ifconfig` :print the ip information
- `su`	/switch user/ :
- `whoami` /who am i/:print this username
- `passwd` [username] /change user password/
- `useradd `	     /add a new account/
- `userdel `[username] /deleate user account/
- `usermod `	     /change user's atraction/
- `groupadd` [groupname] /add a new group/
- `groupdel` [groupname] /deleate group/
- `groupmon` 		/change group's attraction/
- `newgrp` [groupname]	/switch to anthor group/
- `df`                  /sprint the diskusesize/
- `du
- `fdisk`    /divsion the disk/
- `vim`
- `yum`
- `curl` 查看网络内容
- `scp`#`scp -r /root/lk root@106.14.167.5:/home/admin` 把本地lk文件复制到远程的admin文件夹下
ctrl_shift_f


