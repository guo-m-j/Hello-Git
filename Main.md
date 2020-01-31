## 一些基本概念及对应翻译
* 仓库（Repository）
* 收藏（Star）
* 复制克隆项目（Fork）
* 发起请求（Pull Request）
* 关注（Watch）
* 事务卡片（Issue）

## 用于Git Bash的常用命令
### 1.配置部分  

> ssh-keygen -t rsa -C "your_email@youremail.com" 

该命令用于在本地创建ssh key，输入完毕后，使用默认的一路回车。最后会在~/下生成.ssh文件夹，进去，打开id_rsa.pub，复制里面的key。 
再回到github上，进入 Account Settings（账户配置），左边选择SSH Keys，Add SSH Key,title可以随便填，在下面框中粘贴在你电脑上生成的key即可。

---
> ssh -T git@github.com

该命令用于验证是否连接成功。输入yes就会看到：You've successfully authenticated, but GitHub does not provide shell access。
这就表示已成功连上github。 

---
> git config --global user.name "your name"  
> git config --global user.email "your_email@youremail.com"

该命令用于设置Username和Email，用于每次的Commit。

---
> git init

该命令用于在当前文件夹内初始化Git，可以用`cd /your workplace`的方式给仓库在本地定位

---
### 2.对本地仓库的几个操作

（1）用于添加：
> touch filename            &emsp; # 创建某文件到工作目录  
> git add filename          &emsp; # 添加该文件到暂存区  
> git commit -m  'note'     &emsp; # 添加该文件到仓库，注释为'note'  
> git push origin master    &emsp; # 将修改后的仓库上传到github  
---

（2）用于删除：
> rm -rf filename           &emsp; # 在当前工作目录删除某文件  
> git rm filename           &emsp; # 在暂存区删除该文件  
> git commit -m  'note'     &emsp; # 在仓库中删除该文件，注释为'note'  
