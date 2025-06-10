# github工作流 
_呵呵,这是瓦塔西第一次正式使用github.虽然之前已经做过小组作业了但是当时使用github的方式十分原始喵.感谢老大指点学习方向!
接下来是几个常见git语句的自我科普.谨防自己忘记._
- 仓库
- 操作代码的平台
  
---

## 仓库
_一个仓库就是一个项目的文件夹，**包含了所有代码文件和版本记录**_
- 远程仓库(gituhub)
- 本地仓库

```python
def greet():
    print("Hello, Markdown!")
```
## Git 基本工作流流程图
    远程仓库（GitHub、Gitee等）

        ↑               ↓
         
    git push         git pull
    
        ↑               ↓
        
本地仓库 ← git commit ← 暂存区 ← git add ← 工作区（改代码）

### git 指令
_有几个基础的需要先掌握: git init,git 
Git 命令在终端中作用的是“你当前所在的目录”，而不是“整个项目”或“IDE 中看到的所有文件
### git init
  该指令会让你本地的一个普通项目文件夹变成git仓库
### git add
  该指令将文件加入暂存区
  ```bash
  git add 文件名.py # 或添加所有更改
git add .
```
### git status
  该指令会列出：
  1. 新增但未追踪的文件（Untracked files）
  2. 修改过但未提交的文件（Changes not staged for commit）
 #### pwd
   该指令会显示你在哪个目录搞这些仓库兮兮的
### git commit
该指令会把缓存区的内容提交到本地仓库
```bash
git commit -m "(提交说明,写完会显示在git仓库头顶的一些说明)xx文件已上传"
```
### git push
该指令把你的仓库和远程仓库相连.
```bash
git push origin main
```
这里的**origin** 是你给远程git仓库取的名字.**main** 是你本地这个仓库的名字

### git pull
```bash
git pull origin main
```
该指令从远程仓库里拉取最新代码.因为别人可能在git仓库更新了你之前传过去的代码,所以你再拉下来到你本地的就是更新过后的,新的内容会合并到你的本地项目里.
hint: 每天写代码前建议先 git pull，防止冲突
###  git remote
```bash
git remote -v           # 查看远程仓库
horigin  git@github.com:Tanya050831/git-work.git (fetch)
origin  git@github.com:Tanya050831/git-work.git (push)
(显示你的git仓库)
git remote add origin2 https://github.com/xxx.git
(添加一个新的仓库)
```
该命令告诉本地终端Git 远程仓库在哪，push/pull 都需要这个地址(的名字:origin 2)

### git branch 
该命令为新功能创建分支
```bash
git branch              # 查看所有分支
git branch 分支a # 创建 分支a 分支
git checkout 分支a # 切换到 分支a 分支
```
_或者一步到位_
```bash
git checkout -b feature/login-page ## 从主分支创建并切换到新分支
```
以我自己的尝试为例子.在进行如下操作后,前面的主运行目录(带*号)变成了 branch
```bash
(venv) tuchen@TuchendediannaodeMacBook-Air github % git checkout -b gogogitwotamalaila
Switched to a new branch 'gogogitwotamalaila'
(venv) tuchen@TuchendediannaodeMacBook-Air github %  git branch
* gogogitwotamalaila
  main
```

进入新分支目录后开始在新目录里构建代码
提交更改.注意add和commit都要写不然代码还在缓存区,本地仓库(分支)会收不到这个代码
```bash
git add .(xxx.py,或者啥也不写,那就是全加?)
git add src/github_b.py(如果代码不在你目前运行的目录下,那么你添加的时候写上明确的路径)
git commit -m "Add github_b.py"
```
当你打开终端时，它默认打开在 **项目根目录**（通常是 Git 仓库的根目录）
但你也可能在某个子目录点开终端，这时终端就是从那个**子目录**开始的

把分支和远程仓库绑定
```bash
 git push -u origin gogogitwotamalaila
```
### git clone : 把远程仓库的代码下载到本地
```bash
cd ~/projects
git clone https://github.com/teammate-user/project-repo.git
cd project-repo
```

### git clone
```bash
cd ~/projects
git clone https://github.com/teammate-user/project-repo.git
cd project-repo
```

```

