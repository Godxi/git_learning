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
查看所有日志：$ git log
a. git log 的常用选项：

-p		按补丁格式显示每个更新之间的差异。
--stat		显示每次更新的文件修改统计信息。
--shortstat	只显示--stat中最后的行数修改添加移除统计。
--name-only	尽在提交信息后显示已修改的文件清单。
--name-status	显示新增 修改 删除的文件清单。	  
--abbrev-commit	仅显示SHA-1的前几个字符，而非所有的40个字符。
--relative-date	使用较短的相对时间显示（如：2 weeks ago）。
--graph		显示ASCII图形表示的分支合并历史。
--pretty	使用其他格式显示历史提交信息。

b. 限制git log 输出的选项：

-(n)		仅显示最近的n条提交
--since,--after	仅显示指定时间之后的提交
--since,--before仅显示指定时间之前的提交
--author	仅显示指定作者的提交
--committer	仅显示指定提交者的提交
--grep		仅显示含指定关键字的提交
-S		仅显示添加或移除了某个关键字的提交

c. 查看提交历史 各个分支的指向以及项目的分支分叉情况
$ git log --oneline --decorate --graph --all


































