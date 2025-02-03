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

