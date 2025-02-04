# DAY1

1. 了解Git是什么，它如何帮助版本控制代码。

2. GitHub是实习Git的工具：托管代码、协作、版本控制。

3. 下载并安装Git

   mac 用户  

   先使用Terminal 安装Homebrew  

   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

   安装git

   brew install git

   检查Git是否成功安装

   git --version

4. 配置git

   git config --global user.name "你的名字"

   git config --global user.name "你的名字"

5. 注册并了解GitHub界面

   在GitHub上创建一个仓库并将其克隆到本地

   注意版本保护协议

   git clone https://github.com/你的用户名/仓库名.git

6. 配置GitHub仓库并提交更改

   进入仓库的根目录，打开Terminal，创建一个名为 `README.md` 的文件

   echo Hello, GitHub!  > README.md

   添加文件到暂存区

   git add README.md

   **提交更改**：

   git commit -m "Initial commit"

   **推送更改到GitHub仓库**

   git push origin master/main

7. 通过 SSH 进行认证

   生成 SSH 密钥：在终端输入以下命令

   mkdir -p ~/.ssh

   chmod 700 ~/.ssh

   ssh-keygen -t rsa -b 4096 -C "your_email@example.com"

   添加 SSH 密钥到 GitHub

   eval "$(ssh-agent -s)"
   ssh-add ~/.ssh/id_rsa

   复制公钥内容：

   cat ~/.ssh/id_rsa.pub

   将公钥添加到 GitHub：

   1. 登录到 GitHub。
   2. 进入 **Settings** > **SSH and GPG keys**。
   3. 点击 **New SSH key**，粘贴公钥，点击 **Add SSH key**。

​                使用 SSH 进行推送： 在将远程仓库的 URL 更改为 SSH 格式：

​		git remote set-url origin git@github.com:stch66/xjpmathTE.git

# DAY2

1. 如何将本地删除的文件同步到 GitHub：

   **删除文件**（你已经完成了这一步）

   通过 Git 告知删除操作 

   git rm READM2E.md

   **提交更改**： 删除操作添加到暂存区后

   git commit -m "delete READ2E.md"

   推送更改到 GitHub

   git push origin main"

2. 查看状态与提交

   修改`README.md`文件内容：

   echo "Learning Git and GitHub!" >> README.md

   查看状态并提交更改：

   git status
   git add README.md
   git commit -m "Updated README"
   git push origin main

3. 学习分支管理

   创建并切换到一个新分支

   git checkout -b new-feature

   修改并提交文件：

   echo "This is a new feature" > feature.txt
   git add feature.txt
   git commit -m "Added new feature"
   git push origin new-feature

4. 合并分支

   切换回主分支并合并分支：

   git checkout main
   git merge new-feature

   暂存更改

   git stash

   恢复暂存的更改

   git stash pop

# Day 3















