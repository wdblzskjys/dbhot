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

Git config --list 查看一些配置信息

注意这个name和邮箱只起到标识用户身份作用，和代码托管平台的邮箱和密码无关

git config --global user.name "Your Name"
git config --global user.email "your_email@example.com"

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

![image-20230715124329566](C:\Users\减肥的小胖子\AppData\Roaming\Typora\typora-user-images\image-20230715124329566.png)

现在处于3.0版本，我要开发商城功能，创建一个开发分支去开发商城，但是开发到中途，线上版本出现bug,那么需要紧急修复Bug,则在3.0版本基础上创建一个修复bug分支，修复完成之后合并到主分支

不同分支之间是隔离的 

分支相关命令：

查看分支

git branch 

创建分支

git branch 分支名称

切换分支 

git checkout 分支名称

分支合并（可能产生冲突）

git merge 要合并的分支

注意:切换分支再合并 比如现在dev分支想要合并到master分支，需要切换到master分支

删除分支 

git branch -d 分支名称

# 7.git工作流

![image-20230715125251717](C:\Users\减肥的小胖子\AppData\Roaming\Typora\typora-user-images\image-20230715125251717.png)

开发代码写在dev分支，等到功能认为可以了，再合并到主分支

主分支上版本都是稳定版本

# 8.关于代码托管仓库

![image-20230715130312299](C:\Users\减肥的小胖子\AppData\Roaming\Typora\typora-user-images\image-20230715130312299.png)

查看远程仓库的地址

   `$ git remote -v                                                                  origin  https://github.com/wdblzskjys/dbhot.git (fetch)                          origin  https://github.com/wdblzskjys/dbhot.git (push)                          `    

Git仅允许为每个远程仓库设置一个 “origin”。如果你尝试再次添加 “origin”，就会出现该错误。

git remote set-url origin "新的远程仓库地址"

覆盖原来的origin地址

关于认证:setting->developer settings->tokens->![image-20230715203610562](C:\Users\减肥的小胖子\AppData\Roaming\Typora\typora-user-images\image-20230715203610562.png)

生成token 在第二次要输入Openssh password for github的时候 填入这个token即可

提交     `$ git push -u origin main`    

![image-20230715210622312](C:\Users\减肥的小胖子\AppData\Roaming\Typora\typora-user-images\image-20230715210622312.png)

登录不成功就把相关的凭据删除再试一试

# 9.关于github的使用

1.给远程仓库起别名

git remote add origin 远程仓库地址

2.向远程推送代码

git push -u origin 分支

3.克隆远程仓库的代码

git clone 远程仓库地址

4.切换分支

git checkout 分支

# 10.git协同开发
