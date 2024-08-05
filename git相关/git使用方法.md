在Bash运行以下命令配置用户名和电子邮件地址：

```bash
git config --global user.name "Your Name"
git config --global user.email "your_email@example.com"
```

运行以下命令来初始化一个新的 Git 仓库：

```bash
git init
```

使用以下命令将项目文件添加到 Git 仓库：

```bash
git add .
```

运行以下命令提交您的更改到本地仓库，并添加一条提交消息：

```bash
git commit -m "Initial commit"
```

回到 GitHub 上新创建的仓库页面，复制仓库的 URL。然后，运行以下命令将本地仓库连接到远程 GitHub 仓库：

```bash
git remote add origin repository_url
```

最后，使用以下命令将您的更改推送到 GitHub 仓库：

```bash
git push -u origin main
```

###### 如果提示：error: src refspec main does not match any

实际就是如果把github上文件先下载在本地，再创建git目录，会将分支命名为master，而clone到本地分支会命名为main，这要提交会出错，这时候需要改名。你的本地Git客户机在你使用git init初始化repo时创建了一个名为master的默认分支，但是GitHub上的远程存储库没有master，而默认分支称为main。
解决办法1-将分支命名为master

```bash
git push -u origin master
```

而不是git push -u origin main

或者解决办法2-把分支命名为main
在 git push -u origin main之前运行再push一下

```bash
Run git checkout -B main 
```