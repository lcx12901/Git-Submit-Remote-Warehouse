# Git提交项目基本操作
## 创建用户及邮箱
```
# 全局设置用户名及邮箱
git config --global user.name "xxx"
git config --global user.email xxxxx.com
```

## 创建项目
### 方式一：本地创建
```
mkdir project  # 手动创建项目文件夹
cd project # 进入文件夹
git init # 初始化代码仓库
```
### 方式二：克隆远程仓库
```
cd Desktop/  # cd进入存放项目的文件夹
git clone http://xxx.git  # 克隆
cd project  #进入项目文件夹
git init  # 初始化项目
```
## 添加远程仓库
```
git remote add origin http://xxx.git # 添加远程仓库，远程仓库名为origin
```
## 拉取远程仓库
```
git pull origin master  # 拉取名为origin的远程仓库合并到本地master分支
```
## 代码添加与提交
```
git add * ##提交暂存所有
git commit -m 'xxx' ##完成提交并写入提交内容
git status ##显示提交状态
git push origin master # 推送本地master分支到远程仓库
```


## 代码差异错误使用：消除本地README.md与远程仓库的差异
```
git pull origin master --allow-unrelated-histories
重新add和commit README.md
git push origin master
```


# npm篇
## 加速npm下载
```
npm install --registry=https://registry.npm.taobao.org
```
