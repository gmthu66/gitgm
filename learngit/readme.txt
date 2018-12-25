#lerngit readme.txt

Git is a version control system
Git is free software

The tutorial as belong:
https://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000/0013743256916071d599b3aed534aaab22a0db6c4e07fd0000

1.mkdir <文件名>
初始化一个Git仓库，使用git init命令（仓库中也是可以新建文件夹）。

添加文件到Git仓库，分两步：

使用命令git add <file>，注意，可反复多次使用，添加多个文件；
使用命令git commit -m <message>，完成

2.如果对于原来的文件又做了修改
git status命令可以让我们时刻掌握仓库当前的动态，显示是否有没有准备提交的修改
git diff命令可以让我们查看具体修改了什么内容，eg：git diff readme.txt
知道对 readme.txt 作了什么修改后，就可以再次把它移交到仓库了：git add readme.txt
然后看一下仓库状态 git status
然后放心提交 git commit "修改说明"
提交后再使用 git status 查看一下仓库状态
