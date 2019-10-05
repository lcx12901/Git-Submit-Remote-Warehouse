# test
## push an existing repository from the command line
、、、
git remote add origin git@github.com:lcx12901/xxx.git
git push -u origin master
、、、
## 消除本地README.md与远程仓库的差异，避免报错
、、、
git pull origin master --allow-unrelated-histories
重新add和commit README.md
git push origin master
、、、
