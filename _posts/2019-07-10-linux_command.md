---
layout: post
title: 'Linux命令行初探'
date: 2019-07-10
author: 'Hao Wong'
tags: Linux 
---
来源:印象笔记．时间:2017/11/18  
基本命令：  
pwd    输出当前目录  
cd 目录名    切换至指定目录  
		./ 表示当前目录  
		../ 表示父目录  
ls     输出当前目录下所有项目  
touch 文件名    新建文件  
mkdir 目录名    新建文件夹  
rmdir 目录名     删除文件夹  
cp 项目1 项目2   复制项目1至项目2  
mv 项目1 项目2  移动项目1至项目2 ，若路径相同则为重命名  
rm 文件名     删除文件  
ln 项目1 项目2   为项目1创建硬链接项目2  
ln -s 项目1 项目2    为项目1创建软链接项目2  
su  切换至管理员权限  
sudo  命令1 ，命令2….   以管理员权限运行命令1,命令2….  
cat文件名 输出文件文本  
chmod xxx 项目 修改该项目权限  
		-r 对目录下所有文件执行相同操作  
		u+x 给予用户组以执行权限  
		u-x 取消用户组执行权限  
mount -t type device directory挂载移动存储设备  
		type 指定文件系统类型 可选项为vfat,ntfs,iso9660  
		device 设备文件的位置  
		directory 挂载点在虚拟目录的位置  
umount [directory |device]  

ps 查看进程信息  
	-A 所有进程  
	-f 显示完整格式信息  
	-j显示任务信息  
top 查看进程  
kill+进程号 关闭进程  
killall+进程名 关闭进程   
ipcs 查看当前共享内存段  
printenv 查看全局变量  
set 显示局部变量  
export 局部变量名  导出局部变量至全局  
unset 变量名   删除局部变量  
mytest=(one two three) 设定环境变量数组  
echo ${mytest[2]} 显示mytest 变量的第三个元素  
将2换为*即可显示所有元素  
alias name =’ alias’使用命令别名  
		-p 显示已有别名  

; 分号可连接多个命令  
#！/bin/bash 脚本文件首行需添加此语句  

echo 输出至终端  
	-n 	使下一行合并至上一行显示  
test=`date` 将date命令结果输出至test  

command > outputfile 输出重定向（覆盖源文件）  
command >> outputfile 输出重定向（追加）  
df 查看磁盘剩余空间  
	 -h 适应大小显示  
du 显示当前目录所占空间  
	-c 显示所有已列出文件的总大小  
	-h 适应大小显示  
	-s 显示总计大小  

sort 对该文本文件的数据按文本方式排序（不改变源文件）  
	-n 按值排序
	-M 按月排序
	-m 将两个已排序文件排序
	-k 指定排序位置开始排序
	-t 指定分隔符显示

grep [option] pattern [file] 在指定文件搜索数据  
		-v 反向搜索
		-n 显示搜索结果的行号
		-c 显示结果数
		-e 搜索多条数据

压缩数据：  
	bzip2 压缩为bz2格式，完成后删除源文件
	bunzip2 解压bz2格式文件
	bzcat 显示压缩的文本文件的内容
	bzip2recover 尝试修复bz2文件
	gzip,gzcat,gunzip与上类似，对应gz格式
	zip  压缩为zip格式
	zipsplit 分卷压缩
	unzip 解压文件
	tar function [options] object1 object2 …
		tar -zxvf filename.tgz  解压tgz文件
		tar -xvf filename 解压tar文件
		tar -tf 列出tar文件内容
		tar -cvf  test.tar dir1/ dir2/  创建包含dir1和dir2的tar文件

