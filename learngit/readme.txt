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


2.如果对于原来的文件又做了修改怎么提交？

git status命令可以让我们时刻掌握仓库当前的动态，显示是否有没有准备提交的修改
git diff命令可以让我们查看具体修改了什么内容，eg：git diff readme.txt
知道对 readme.txt 作了什么修改后，就可以再次把它移交到仓库了：git add readme.txt
然后看一下仓库状态 git status
然后放心提交 git commit "修改说明"
提交后再使用 git status 查看一下仓库状态


3.保存快照（Git中称为commit）与版本控制

在打Boss之前，会手动存盘，以便万一失败可以从最近的地方开始。当文件修改到一定程度的时候，就可以“保存一个快照”
Git中称为commit，一旦文件改乱了或者误删了文件，还可以从最近的一个commit恢复然后继续工作

首先回顾下readme.txt有几个版本提交到了git仓库中：
用git log命令查看

若准备把 readme.txt 回退到上一个add tutorial那个版本：
使用git reset 命令： git reset --hard HEAD^
然后查看 readme.txt 的内容是否回退： cat readme.txt 

如果回退之后想要再回到之前最新的版本？？
git reset --hard <commit id(例如1094a)>
其中版本号不用写全，前几位就可以，Git会自动去找（Git 内部有个指向当前版本的HEAD指针）

如果没有不知道版本号在哪里？？
git reflog 用来记录每一次命令，可以查看到对应的每次 git commit 对应的版本号