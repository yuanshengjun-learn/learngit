Git is a distributed version control system.
Git is free software.

//1、创建版本库
$ mkdir "<文件夹名称>"
$ cd "<文件夹名称>"
$ pwd
//pwd命令用于显示当前目录

//2、将创建的目录变成Git可以管理的仓库
$git init

//写文件放入仓库目录下（或其子目录下）
//第一步，用命令git add告诉Git，把文件添加到仓库：
$ git add readme.txt
$ git add readme1.txt
$ git add readme2.txt

//第二步，用命令git commit告诉Git，把文件提交到仓库：
$ git commit -m "<提示信息>"
//-m后面输入的是本次提交的说明

//commit可以一次提交很多文件，所以你可以多次add不同的文件
$ git add file1.txt
$ git add file2.txt file3.txt
$ git commit -m "add 3 files."


//修改文件后可以通过git status命令查看结果，git status命令可以让我们时刻掌握仓库当前的状态
//git diff命令查看具体修改
//然后再重新添加重新提交

git log命令显示从最近到最远的提交日志

要把当前版本append GPL回退到上一个版本，$ git reset --hard HEAD^
查看内容：$ cat readme.txt
Git提供了一个命令git reflog用来记录你的每一次命令：

HEAD指向的版本就是当前版本，因此，Git允许我们在版本的历史之间穿梭，使用命令git reset --hard commit_id。
穿梭前，用git log可以查看提交历史，以便确定要回退到哪个版本。
要重返未来，用git reflog查看命令历史，以便确定要回到未来的哪个版本。


场景1：当你改乱了工作区某个文件的内容，想直接丢弃工作区的修改时，用命令git checkout -- file。
场景2：当你不但改乱了工作区某个文件的内容，还添加到了暂存区时，想丢弃修改，分两步，第一步用命令git reset HEAD <file>，就回到了场景1，第二步按场景1操作。
场景3：已经提交了不合适的修改到版本库时，想要撤销本次提交，参考版本回退一节，不过前提是没有推送到远程库。