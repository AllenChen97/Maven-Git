# [Git](https://www.bilibili.com/video/BV1FE411P7B3)

## 1. 简介

### 1.1. SVN和Git区别
- git是分布式管理系统，没有中央服务器，每个人的电脑都是完整的版本。团队中A修改的文件，则会推送给所有人

### 1.2. 历史
linux之父 因BitKeeper中止和 linux内核社区的免费使用权 开发出自己的版本管理系统

## 2. 命令
```shell
# 查看系统配置
git config --system --list

# 查看当前用户(global)配置
git config --global --list

# 设置当前用户(global)配置
git config --global user.name JinzhaoChen
git config --global user.email j.chen88@newcastle.ac.uk
```

## 3. 命令

### 3.1. 提交
建立项目
- 新建
```shell
git init
```

- 远程克隆
```shell
git clone
```

### 3.2. 提交
1. 工作目录 Working Directory

2. 暂存区 History
```shell
git add . # 提交后状态变为暂存 staged
git checkout # 丢弃修改，变回 unmodify状态
```

3. 资源库 Stage
```shell
git commit
git reset HEAD filename # 撤回 提交，版本指针HEAD
```

4. 远端 Remote Directory
```shell
git push origin master
git pull
```

### 3.3. 忽略文件
主目录下建立.gitignore文件
- *.txt 所有txt文件
- /temp 目录上的所有文件，不包含temp
- temp/ 目录下的所有文件，不包含temp以外的
- temp/*.txt 目录下的所有txt文件


## 4. 分支
- 创建/删除分支
```shell
git branch dev

git branch -d dev # 本地分支
git push origin --delete dev # 远程分支

```

- 切换分支
```shell
git checkout -b dev
```

- 合并指定分支到当前分支
```shell
git merge dev # 假设目前是在 master主分支上
```