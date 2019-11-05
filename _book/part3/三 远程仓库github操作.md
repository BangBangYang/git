# 三 远程仓库github操作

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

