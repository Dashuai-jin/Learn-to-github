
## 通过git提交到github
push：该单词直译过来就是“推”的意思，如果我们本地的代码有了更新，为了保持本地与远程的代码同步，我们就需要把本地的代码推到远程的仓库，代码示例：
```bash
git push origin main
```
pull：该单词直译过来就是“拉”的意思，如果我们远程仓库的代码有了更新，同样为了保持本地与远程的代码同步，我们就需要把远程的代码拉到本地，代码示例：
```bash
git pull origin main
```
![alt text](image.png)
## 步骤
1. 首先我们需要在github上创建一个新的仓库，假设我们创建的仓库名称为my-repo。
2. 然后我们在本地创建一个新的文件夹，并进入该文件夹
3. 接下来我们需要初始化一个新的git仓库
```bash
git init # Initialize a new git repository
```
4. 然后我们需要将该文件夹与我们在github上创建的远程仓库关联起来
```bash
git remote add origin "远程仓库地址"

git remote -v # Verify new remote

git remote set-url origin "远程仓库地址" # Change remote URL

git remote remove origin # Remove remote

```
5. 接下来我们可以在该文件夹中创建一些文件，并将这些文件添加到git的暂存区
```bash
git add .
```
6. 然后我们需要提交这些文件到本地的git仓库
```bash

# 提交是可以新建分支的
git branch #查看本地分支

git checkout -b newbranch #新建并切换到newbranch分支

git branch -M main #重命名本地分支为main

#在某个分支开发新的功能，开发完成后合并到主分支
git checkout main #切换到主分支
git merge newbranch #将newbranch分支合并到main分支

#使用rebase方式合并分支
git checkout main #切换到主分支
git rebase newbranch #将newbranch分支的修改应用到main分支上

#删除提交的分支
git branch -d newbranch #删除newbranch分支
#提交到本地仓库
git commit -m "Initial commit" #引号内是本次提交的说明，-m表示message
```
7. 最后我们可以将本地的代码推送到远程的github仓库
```bash
#分支名称可能是main或者master，具体以你创建的远程仓库为准

git push origin master:main #如果本地分支是master，远程分支是main

git push -u origin master #默认推送

git push -f origin master:main #强制推送
```
注意：如果是第一次推送代码到远程仓库，可能会提示需要输入github的用户名和密码，或者需要使用token进行身份验证。

## 拉取
如果远程仓库有更新，我们可以使用pull命令将远程的代码拉取到本地
```bash 
git pull origin main --allow-unrelated-histories #如果本地分支是main，远程分支是main

git pull origin master --allow-unrelated-histories #如果本地分支是master，远程分支是main


```
