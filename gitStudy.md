# GIt知识点

## Git主要分为四个工作区:

```shell
workspace工作区
index/stage缓存区
repository 仓库区 
remote远程仓库
```

## Git基本命令

```sh
git clone 项目地址 # 克隆网络上的项目
git init 初始化一个git项目
git add 路径+文件名 # 添加具体修改文件
git add . # 添加所有修改的文件代码
git commit -m '表明这次修改的内容'  
git push origin 分支名
git pull  拉取该分支最新代码
git reset 
git checkout
```

## 工作流程

```text
1.在工作中目录添加,修改文件
2.对需要进行版本管理的文件放入缓存区
3.将暂存区的文件提交到git仓库
因此,git管理的文件存在三种状态:已修改(modified) 已缓存(staged) 已提交(committed)
```



## 本地仓库搭建

```text
1.当前目录新建一个git代码库 :git init
2.克隆远程仓库 git clone [url] + 网址
```

## 需要忽略的文件

```text
主目录下的.gitignore文件
```

## 使用码云gitee

```text
创建账号,新建远程仓库
```

## git分支

```text
主分支master,一般情况下不允许在上面工作,可以在新建的dev分支上工作
```

```sh
git branch    #列出所有本地分支
git branch -r #列出所有远程分支
git branch [branch-name] #新建一个分支,但是依旧停在当前分支
git checkout -b [branch] #复制一份,并切换到新分支
git merge [branch] #合并指定分支(branch)到当前分支
git branch -d [branch-name] #删除分支
git push origin -- delete [branch-name] 
git branch -dr [remote/branch] #删除远程分支
```

## 将本地项目上传到gitee远程仓库

```sh
git init #初始化
git remote add origin https://gitee.com/个人网址 #连接到远程仓库,之后才能push
git pull origin master #拉取远程master分支(修改之前)
git add . #加入暂存区
git commit -m '修改记录' #把修改的加入本地仓库
git push origin master #提交到gitee远程仓库
git push origin master -f #提交时产生冲突,保留线上的文件,强制推送命令(通常不用)
git push origin master #保留线上的readme文件
```

## 从已有仓库拉取项目提交代码

![1662399069989](C:\Users\17436\Desktop\ygl\document\git\gitStudy.assets\1662399069989.png)



## 修改代码提交

![1662399308049](C:\Users\17436\Desktop\ygl\document\git\gitStudy.assets\1662399308049.png)

## 发生冲突

```java
不会 呜呜呜
```

## 团队协作

```text
团队协作/跨团队协作
1、团队 clone
本地库push到远程仓库，其他人clone即可拉取使用，修改完push回远程仓库。自己用时，pull拉回来使用。
2、跨团队 远程库之间用fork叉子之后再clone
AB两个远程库之间A用fork叉子给B，B再用clone到本地库使用，修改完push到B，再对A发出pull request，A审核后合并merge，A再pull拉回去使用。
```

