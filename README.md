# Git提交项目基本操作（排错指南）
##创建用户及邮箱
```
$ git config --global user.name "xxx"
$ git config --global user.email xxxxx.com
```
##文件git初始化
```
$ git init
```
##代码提交
```
git add * ##提交暂存所有
git commit -m 'xxx' ##完成提交并写入提交内容
git status ##显示提交状态
```
## SSH
### 生成密钥
```
ssh-keygen -t rsa -C "xxxxx@xxxxx.com邮箱账号" 
```
### 查看秘钥
```
cat ~/.ssh/id_rsa.pub
```
### 复制查看到的秘钥到setting中“SSH and GPG keys” ——》 “Add SSH key”
### 测试 ssh 链接 github
```
ssh -T git@github.com
```
## push an existing repository from the command line
```
git remote add origin git@github.com:lcx12901/xxx.git
git push -u origin master
```
## 遇到“ssh: connect to host github.com port 22: Connection refused”的问题，办法如下：
### 打开存放ssh的目录
```
cd ~/.ssh
ls
```
### 查看是否存在 id_rsa   id_rsa.pun  known_hosts 三个文件，没有上面生成
### 存在，则新建config文件输入下面内容
```
Host github.com
User 1367372276@qq.com
Hostname ssh.github.com
PreferredAuthentications publickey
IdentityFile ~/.ssh/id_rsa
Port 443
```
### 保存之后再次执行"ssh -T git@github.com"时，会出现如下提示，回车"yes"即可

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
