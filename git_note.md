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

![](/images/git_cheat.jpg)