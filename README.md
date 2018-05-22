git 学习笔记之常用命令：
1.当安装完git应该做的第一件事就是设置你的用户名称与邮件地址。这样做很重要，因为每一个git提交都会使用这些信息，并且他会写入到你的每一次提交中，不可更改：
$ git config --global user.name "hlx"
$ git config --global user.email hlx@example.com
对于使用了 --global 选项，那么该命令只需要运行一次，因为之后无论你在该系统上做任何事情，Git都会使用那些信息。当你想针对不同的项目使用不同的用户信息时请运行不带global选项的命令来配置。

检查配置信息：$ git config --list
检查单个配置的信息：输入git config <key>   $ git config user.name
