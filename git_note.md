# Git note

## git 安装和配置(Ubuntu)

* 安装

```bash
sudo apt install git
```

* 配置名字和邮箱

  ```bash
  git config --global user.name "yourname"              # 替换为GitHub用户名
  git config --global user.email youremail@XXX.com      # 替换为GitHub的注册邮箱
  
  #####
  git config --list									  # 查看配置信息
  git config user.name								  # 查看已经配置的用户名
  git config user.email								  # 查看已经配置的邮箱
  ```

* 生成key

  ```bash
  ssh-keygen -t rsa -b 4096 -C "your_email@example.com"   # 替换为GitHub的注册邮箱
  ```

  > 输出：
  >
  > Generating public/private rsa key pair.
  > Enter a file in which to save the key (/home/you/.ssh/id_rsa): [Press enter]
  >
  > Enter passphrase (empty for no passphrase): [Type a passphrase]
  > Enter same passphrase again: [Type passphrase again]

* 将key加入到github中

  ```bash
  cat ~/.ssh/id_rsa.pub   # cat查看保存key的文件
  ```

  到github网站：Setting -> SSH and GPG keys -> New SSH key，复制查看到的所有内容到Key中，Title随意取啦，eg: my Ubuntu 18.04



## git cheat sheet

![](https://github.com/zcgeqian/notes/raw/master/images/git_cheat.jpg)



## git 目录权限问题

在使用git相关命令进行项目管理时，发现“权限不足”的报错问题，查找后发现部分文件和文件夹的用户和组为root用户，使用chmod命令更改文件夹的用户和组为当前用户和组即可：

`chmod -R 用户名:用户组名 foldername `

其中，`－Ｒ`表示递归的完成



## git 分支相关操作

* 创建并切换到指定分支

  `git checkout -b dev`

  该命令相当于执行了：

  `git branch dev`  //创建分支

  `git checkout dev`　//切换分支

* 合并和删除分支

  将其他分支的修改更新到主分支上使用命令，合并前需先切换到主分支：

  `git merge dev`

  删除`dev`分支：

  `git branch -d dev`

