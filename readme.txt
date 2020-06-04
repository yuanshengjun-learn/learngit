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


//修改文件后可以通过git status命令查看结果