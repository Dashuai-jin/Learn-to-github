
## 通过git提交到github
push：该单词直译过来就是“推”的意思，如果我们本地的代码有了更新，为了保持本地与远程的代码同步，我们就需要把本地的代码推到远程的仓库，代码示例：
```bash
git push origin main
```
pull：该单词直译过来就是“拉”的意思，如果我们远程仓库的代码有了更新，同样为了保持本地与远程的代码同步，我们就需要把远程的代码拉到本地，代码示例：
```bash
git pull origin main
```

1. 首先我们需要在github上创建一个新的仓库，假设我们创建的仓库名称为my-repo。
2. 然后我们在本地创建一个新的文件夹，并进入该文件夹
3. 接下来我们需要初始化一个新的git仓库
```bash
git init
```
4. 然后我们需要将该文件夹与我们在github上创建的远程仓库关联起来
```bash
git remote add origin
```
5. 接下来我们可以在该文件夹中创建一些文件，并将这些文件添加到git的暂存区
```bash
git add .
```
6. 然后我们需要提交这些文件到本地的git仓库
```bash
git commit -m "Initial commit" 引号内是本次提交的说明
```
7. 最后我们可以将本地的代码推送到远程的github仓库
```bash
git push -u origin main
```
注意：如果是第一次推送代码到远程仓库，可能会提示需要输入github的用户名和密码，或者需要使用token进行身份验证。