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

        ↑           ↓
        
    git push     git pull
    
        ↑           ↓
        
本地仓库 ← git commit ← 暂存区 ← git add ← 工作区（改代码）
