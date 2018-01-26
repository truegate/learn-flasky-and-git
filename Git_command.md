### Git 学习笔记
> Fellow [This](https://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000)

![git](https://cdn.liaoxuefeng.com/cdn/files/attachments/0013848605496402772ffdb6ab448deb7eef7baa124171b000/0)

#### Command
* git init
* git reset --hard commit_id
    * commit_id 可以通过 `git log` `git reflog` 查看
    * 可以用HEAD替换commit_id，`HEAD^` 表示上一个，具体用法有 `HEAD^^` `HEAD~100`
* git log --pretty=oneline
* git status
* git reflog
* git commit -m ""
* git add XXX
* git diff