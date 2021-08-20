# Git提交项目基本操作
## 创建用户及邮箱
```
# 全局设置用户名及邮箱
$ git config --global user.name "xxx"
$ git config --global user.email xxxxx.com
```

## 进入项目文件夹
```
$ cd project
```

## 文件git初始化
```
$ git init
```
## 添加远程仓库
```
$ git remote add origin http://xxx.git   ## 仓库地址
```
## 代码提交
```
git add * ##提交暂存所有
git commit -m 'xxx' ##完成提交并写入提交内容
git status ##显示提交状态
```


## 消除本地README.md与远程仓库的差异，避免报错
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
