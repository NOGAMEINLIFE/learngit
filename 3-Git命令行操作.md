再说Git的命令行之前先说一下Git的结构
# 1. Git结构
## 1.1 Git本地结构
Git在本地有三个名词：本地库，暂存区，工作区
这三个之间的关系如下图：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200517221856748.png)
## 1.2 代码托管中心（也叫远程库）
局域网：私人gitLab服务器
互联网：Github，码云
## 1.3 本地库和远程库
本地库和远程库分为两种操作：团队协作和跨团队协作
### 1.3.1 团队协作
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200517223209867.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3NkdXQ0MDY=,size_16,color_FFFFFF,t_70)
### 1.3.2 跨团队协作
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200517223936808.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3NkdXQ0MDY=,size_16,color_FFFFFF,t_70)
# 2. Git命令行
## 2.1 本地初始化
 - 命令：`git init`
 - 效果：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200517224453261.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3NkdXQ0MDY=,size_16,color_FFFFFF,t_70)
 - 注意：：.git 目录中存放的是本地库相关的子目录和文件，不要删除，也不要胡 乱修改。

## 2.2 设置签名
签名是开发人员的身份证明，就和SVN的用户名差不多的意思，签名也分为项目级别或者叫仓库级别，系统用户级别。当你刚用git的时候是必须要设置系统用户级别的签名
 - 项目级别/仓库级别（仅在当前本库范围内有效）
 	- 设置用户名：`git config user.name namedemo`
 	- 设置邮箱：`git config user.email 0000000@qq.com`  
 	- 信息保存位置：当前仓库的`.git/config文件` ![在这里插入图片描述](https://img-blog.csdnimg.cn/20200517225731781.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3NkdXQ0MDY=,size_16,color_FFFFFF,t_70)
 - 系统用户级别
    - 设置用户名：`git config --global  user.name globaldemo`
 	- 设置邮箱：`git config --global user.email globaldemo@qq.com`
 	- 信息保存位置：`~/.gitconfig文件` 
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200517230140897.png)
 - 注意
	 	这里设置的签名中的**name**和**email** 和github的**name**和**email**没有任何关系
 - 级别优先级
	 	根据就近原则，如果有项目级别签名优先使用项目级别签名，没有则使用系统用户级别。

但是一般我们都是把用户名和邮箱都写成github上注册的，看到这个图就明白了：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200517230843417.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3NkdXQ0MDY=,size_16,color_FFFFFF,t_70)
## 2.3 基本操作
### 2.3.1 git status 状态查看
查看工作区，暂存区状态

### 2.3.2 git add 添加
### 2.3.3 git commit 提交
### 2.3.4 git log 查看历史记录
## 2.4 分支管理

 