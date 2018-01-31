## Git 学习笔记
> Fellow [This](https://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000)

![git](https://cdn.liaoxuefeng.com/cdn/files/attachments/0013848605496402772ffdb6ab448deb7eef7baa124171b000/0)

### Command
* git init
* git reset --hard commit_id
    * 版本回溯
    * commit_id 可以通过 `git log` `git reflog` 查看
    * 可以用HEAD替换commit_id，`HEAD^` 表示上一个，具体用法有 `HEAD^^` `HEAD~100`
* git log --pretty=oneline
* git log --graph --pretty=oneline --abbrev-commit
* git status
* git reflog
* git commit -m ""
* git add XXX
* git reset HEAD <file>
    * 撤销暂存区提交的文件，放回工作区
* git checkout -- <file>
    * 用版本库文件替换工作区文件
* git rm <file>
    * 从暂存区删除文件
* git checkout <branch>
* git checkout -b <branch>
    * 创建并切换到分支
    * 相当于 git branch <branch> && git checkout <branch>
* git merge dev
    * 分支合并
* git rm <file>
    * 从暂存区删除文件

### Example

#### Bug 修复
> 手头工作分支任务还没做完，需要对主线进行Debug的情况。
1. 先在手头的分支 `git stash` 工作现场；
2. 再 `git checkout master` 后，`git checkout -b issue-X` 创建 Debug 分支；
3. Debug 完成后，`git checkout master` 回到主分支，`git merge --no-f -m "repair issue-X"` 进行合并，`git branch -d issue-X` 删除Debug分支；
4. 回到之前工作分支后，`git stash pop` 取回保存过的工作现场。