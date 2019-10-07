# test
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
## 消除本地README.md与远程仓库的差异，避免报错
```
git pull origin master --allow-unrelated-histories
重新add和commit README.md
git push origin master
```
