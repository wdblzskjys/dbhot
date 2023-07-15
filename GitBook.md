# 1.版本控制的发展史：

![版本控制的发展史](C:\Users\减肥的小胖子\Desktop\关于Git\版本控制的发展史.png)

## 2.如何使用git进行版本控制

1. 进入要管理的文件夹

2. Git init 让git帮助我们管理当前文件夹

3. Git status 检测当前目录下文件的状态

4. 三种状态的变化

   红色：git未被管理的新文件或者修改的原来的老文件 

​       红色->绿色 git add 文件名 或者.

​      绿色：git已经管理起来 

 5.个人信息的配置 告诉提交版本的是谁 第一次使用配置即可

Git config –global user.email “”

 6.生成版本

->git commit -m ‘msg’    msg为版本的信息

7.git log查看版本信息

#  3.关于git三大区域

![image-20230714223439244](C:\Users\减肥的小胖子\AppData\Roaming\Typora\typora-user-images\image-20230714223439244.png)

 

#  4.版本的快速回滚

git reset --hard 版本号

版本 v1 v2 v3 v4 现在版本v4

回滚到之前版本v2

git log

git reset --hard 版本号

回滚到之后版本 v2->v3

git reflog

git reset -- hard 版本号

![image-20230715105532374](C:\Users\减肥的小胖子\AppData\Roaming\Typora\typora-user-images\image-20230715105532374.png)

# 5.git命令小节

git init 

git add

git commit

git log

git reflog

git reset --hard 版本号

其他的命令补充，三大工作区之间可以通过命令进行转换

![image-20230715110930822](C:\Users\减肥的小胖子\AppData\Roaming\Typora\typora-user-images\image-20230715110930822.png)

# 6.初识分支

紧急修复bug！！！已完成

现在处于3.0版本，我要开发商城功能，创建一个开发分支去开发商城，但是开发到中途，线上版本出现bug,那么需要紧急修复Bug,则在3.0版本基础上创建一个修复bug分支，修复完成之后合并到主分支

不同分支之间是隔离的
