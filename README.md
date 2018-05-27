git 学习笔记之常用命令：
1.当安装完git应该做的第一件事就是设置你的用户名称与邮件地址。这样做很重要，因为每一个git提交都会使用这些信息，并且他会写入到你的每一次提交中，不可更改：
$ git config --global user.name "hlx"
$ git config --global user.email hlx@example.com
对于使用了 --global 选项，那么该命令只需要运行一次，因为之后无论你在该系统上做任何事情，Git都会使用那些信息。当你想针对不同的项目使用不同的用户信息时请运行不带global选项的命令来配置。

检查配置信息：$ git config --list
检查单个配置的信息：输入git config <key>   $ git config user.nam

2.获取Git仓库
有两种方式去的Git项目仓库的方法：
a.现有项目或者目录下导入所有文件到git中 命令：$ git init
b.从服务器克隆一个现有的git仓库 命令：$ git clone [url]
克隆时自定义本地仓库名称：$ git clone [url] [dirname]

3.记录每次更新到仓库
检查当前文件状态：$ git status
跟踪新文件：$ git add <filename>

4.查看已暂存和和未暂存的修改
a.查看尚未暂存的文件更新了哪些部分，不加参数直接输入 git diff：
$ git diff
b.查看已暂存的将要添加到下次提交里的内容，可以用 git diff --cached命令：
$ git diff --cached

5.提交更新：
每次提交前先用git status 查看是否所有改动的文件都已经添加到暂存区了 然后再运行提交命令：
$ git commit

a.提交并添加注释：$ git commit -m '提交注释'
b.跳过使用暂存区域：$ git commit -a -m 'added new benchmarks'
c.移除文件：$ git rm
d.移动文件(重命名)：$ git mv

6.查看提交历史：

我当前是在本地hlx_1分支上面，我想看看 修改了本地hlx_1分支后 推送到远程hlx_1上面后
再切换其他分支 再推送看看效果。
这是hlx_2分支，我改动完此分支后 想push到远程中的hlx_2分支上面，然后和dev-lts分支进行合并
用于模拟供应链的工作流
