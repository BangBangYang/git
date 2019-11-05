### Git基础

####  一 基础操作

![](https://github.com/BangBangYang/imageRepository/blob/master/git%E6%88%AA%E5%9B%BE%E7%AC%94%E8%AE%B0/git%E4%B8%89%E4%B8%AA%E5%8C%BA.png?raw=true)

1. 初始化

```
yangkun@LAPTOP-U72RIU78 MINGW64 ~/Desktop/bigdata/008_Git/git_space/gitProject
$ git init
Initialized empty Git repository in C:/Users/yangkun/Desktop/bigdata/008_Git/git_space/gitProject/.git/

```

2. 配置全局信息(每个工作区提交者都是该用户)

```
yangkun@LAPTOP-U72RIU78 MINGW64 ~/Desktop/bigdata/008_Git/git_space/gitProject (      master)
$ git config --global user.name yangkun

yangkun@LAPTOP-U72RIU78 MINGW64 ~/Desktop/bigdata/008_Git/git_space/gitProject (master)
$ git config --global user.email 1256749651@qq.com

```

文件信息存储路径

```
C:\Users\yangkun\.gitconfig
```

文件内容

```
[user]
	name = yangkun
	email = 1256749651@qq.com
```

3.  从工作区提交至缓存区 

```
git  add  文件名
```

4.  从缓存区提交至版本库

```
git  commit  –m “注释内容”
```

5. 产看文件的状态

```
git  status  
```

6.  查看文件记录

```
执行 git  log  文件名     进行查看历史记录
git log  --pretty=oneline 文件名      简易信息查看
```

7. 回退历史

```
git  reset  --hard HEAD^   回退到上一次提交
git  reset  --hard HEAD~n  回退n次操作
```

8. 版本穿越

```
进行查看历史记录的版本号，执行 
git  reflog  文件名
执行 git  reset  --hard  版本号
```

9. 还原文件

```
git  checkout -- 文件名  
```

10. 删除某个文件

```
先删除文件
再git add 再提交
```

#### 二、 分支

![](https://github.com/BangBangYang/imageRepository/blob/master/git%E6%88%AA%E5%9B%BE%E7%AC%94%E8%AE%B0/%E5%88%86%E6%94%AF.png?raw=true)

1. 创建分支

```
git  branch  <分支名>
git branch –v  查看分支
```

2. 切换分支

```
git checkout  <分支名>
一步完成： git checkout  –b  <分支名>
```

3. 合并分支

```
先切换到主干   git  checkout  master
git  merge  <分支名>
```

**冲突**

•冲突一般指同一个文件同一位置的代码，在两种版本合并时版本管理软件无法判断到底应该保留哪个版本，因此会提示该文件发生冲突，需要程序员来手工判断解决冲突。

**合并时冲突**

•程序合并时发生冲突系统会提示CONFLICT关键字，命令行后缀会进入MERGING状态，表示此时是解决冲突的状态。

![](https://github.com/BangBangYang/imageRepository/blob/master/git%E6%88%AA%E5%9B%BE%E7%AC%94%E8%AE%B0/%E5%90%88%E5%B9%B6%E5%86%B2%E7%AA%81.png?raw=true)

#### 三 远程仓库github操作

![](https://github.com/BangBangYang/imageRepository/blob/master/git%E6%88%AA%E5%9B%BE%E7%AC%94%E8%AE%B0/github%E4%BB%93%E5%BA%93.png?raw=true)

1. 增加远程地址

```
git remote add  <远端代号>   <远端地址> 。
 <远端代号> 是指远程链接的代号，一般直接用origin作代号，也可以自定义。
<远端地址> 默认远程链接的url
例：
git  remote  add  origin  https://github.com/user111/Helloworld.git
```

2.  推送到远程库

```
git  push   <远端代号>    <本地分支名称>。
 <远端代号> 是指远程链接的代号。
 <分支名称>  是指要提交的分支名字，比如master。
git  push  origin  master
```

