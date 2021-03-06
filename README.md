卖假货的学长写给rookies的github入门教程
====
如以下内容有不正确的地方，欢迎指出，非常感谢！部分资源来自网络，侵删！<br>
按卖假货的学长的习惯，先推荐一首歌，再安利一个图，最后上教程，哈哈！<br>
[推荐一首：春天———古巨基](http://music.163.com/#/song?id=86611 "卖假货的学长推荐，点了不后悔，哈哈！") <br>
![](https://github.com/Allen-Liang/github_for_rookies/raw/master/images/nvshen.jpg)<br>
# 1.初识github
## 1.1 github是什么？<br>
>   Github是一个代码托管平台和开发者社区，开发者可以在Github上创建自己的开源项目并与其他开发者协作编码。创业公司可以用它来托管软件项目，开源项目可以免费托管，私有项目需付费。Github主要提供基于Git的版本托管服务，也就是说现在GitHub上托管的所有项目代码都是基于Git来进行版本控制的。<br>
## 1.2 github能干什么？
>	* 这里有世界上最丰富的开源库
> * 这里提供最好的代码托管服务
> * 这里提供最好的团队协作服务 
> * 这里是全球最大的“搞基”（认识大牛）网站 
> * 这里可以搭建个人网站&博客&简历&撩妹（比如：[点点这个，哈哈哈](https://allen-liang.github.io/My_Love/ "撩妹必备，这波不行了！谈学习重要")）
## 1.3 多角度认识github
* 从一般开发者的角度来看，github有以下功能：
> 1.从服务器上克隆数据库（包括代码和版本信息）到单机上。<br>
> 2.在自己的机器上创建分支，修改代码。<br>
> 3.在单机上自己创建的分支上提交代码。<br>
> 4.在单机上合并分支。<br>
> 5.新建一个分支，把服务器上最新版的代码fetch下来，然后跟自己的主分支合并。<br>
> 6.生成补丁（patch），把补丁发送给主开发者。<br>
> 7.看主开发者的反馈，如果主开发者发现两个一般开发者之间有冲突（他们之间可以合作解决的冲突），就会要求他们先解决冲突，然后再由其中一个人提交。如果主开发者> 可以自己解决，或者没有冲突，就通过。<br>
> 8.一般开发者之间解决冲突的方法，开发者之间可以使用pull 命令解决冲突，解决完冲突之后再向主开发者提交补丁。<br><br>

* 从主开发者的角度（假设主开发者不用开发代码）看，github有以下功能：
> 1.查看邮件或者通过其它方式查看一般开发者的提交状态。<br>
> 2.打上补丁，解决冲突（可以自己解决，也可以要求开发者之间解决以后再重新提交，如果是开源项目，还要决定哪些补丁有用，哪些不用）。<br>
> 3. 向公共服务器提交结果，然后通知所有开发人员。<br>

## 1.4 认识github术语
* Git和GitHub
> Git是一个分布式的版本控制系统，与SVN类似；最初由Linus Torvalds编写，用作Linux内核代码的管理。在推出后，Git在其它项目中也取得了很大成功，尤其是在   Ruby社区中，所以目前有很多著名的项目都使用Git进行版本控制。<br>
而GitHub是托管各种git库，并提供一个web界面的一个网站官方地址(https://www.github.com/)<br>可以通过本地的git客户端将自己的代码上传至GitHub可以在GitHub上建立公共库，作为开源软件或个人使用，也可以付费建立私有库，这样就可以作为公司内部软件的代码管理工具。

* Blame
> Git中的“blame”特性描述了文件的每一行的最近一次修改信息，包括修改内容、作者和时间等；可用于追踪某软件新特性的添加及引起bug的提交操作。

* Repository
> 库是GitHub的最基本元素，可想象成本地的项目文件夹；一个库包含所有的项目文件(包括帮助文档)，并保存每个文件的修改历史；库可以有多个合作开发者，也可以作为公共库或私有库的形式开发。

* Private Repository
> 私有库，是指只能被库的创建者或者合作开发者查看并编辑的库，需要付费使用。

* Branch
> 分支是一个库的并行版本，包含在库内，允许独立的开发而不影响现有主分支(primary or master)的运行；当在分支的修改需要发布时，就可以将分支合并(merge)至主分支(master branch)，这样利于多人的分布式开发。

* Pull Request
> 即代码合并请求，由其它开发者或用户向项目的collaborators提议的修改请求，collaborators觉得修改信息合理有效即接受，否则拒绝。

* Merge
> 将一个分支中的修改内容应用到另一个分支的操作就做合并；若两个分支内的修改内容无冲突，则可以通过合并请求(a Pull Request)或命令行(the command line)完成合并操作。

* Clone
> 克隆，是将GitHub上的库文件整个复制到本地主机上，可以实现离线修改，等上线后再同步至Github上的库即可。

* Commit
> 提交信息，或者称为修改信息，是个人提交的对文件的修改记录；

* Fork
> 对其它开发者的库的个人复制，复制的库存在你自己的账户上，你可以自行修改项目内容而不会影响原始的库，也可以将自己的修改通过合并请求(a pull request)的方式请求原始库的开发者更新你的修改。

* Fetch
> 取回，表示从在线的库上获取最新的修改信息而不需要合并代码，取回的代码可以与你本地的分支代码进行比较。

* Push
> 推送，表示将本地的修改内容推送至线上的库，这样其它的开发者就可以通过GitHub网站访问到你的修改内容了。

* Remote
> 远端版本，即类似于GitHub.com的非本地主机的项目版本，可以连接至本地克隆的版本以实现内容同步。

* User
> 用户，指个人注册的GitHub账户，每个用户都可以拥有多个公共库或私有库，也可被邀请加入organizations或称为collaborates。

* SSH Key
> 私钥，是GitHub用以验证你本地主机的身份的，并用此密钥加密传输GitHub网站和你本地主机的数据传输，以保证安全性；这个是需要在“Set up Git”步骤中配置的。

* Organizations
> 组织，即多个开发者组成的团体，可包含众多的库和开发团队。

* Collaborator
> 合作开发者，被库的所有者邀请共同开发某一项目，拥有对库的读写权限。

* Contributor
> 贡献者，对项目有所贡献(如提交代码，修复bug等)的开发者，但不具备合作开发者的访问权限。

* Diff
> 差异，指2个commit或保存的改变间的差异，可以很直观的看出一个文件自上次commit后增加或删除的内容。

* Open Source
> 开源，原指可自由使用、修改和传播的软件，现扩展为一种超越软件的合作哲学，即工件(working materials)在线可用，可被任何人复制(fork)、修改(modify)、讨论(discuss)、并提出修改意见(contribute to)。

* Markdown
> 一种轻量级的标记语言，书写简单，不同于html，无需大量的<tag>就可以实现内容的格式化；GitHub上的众多库中的帮助文档就是这种格式，如README.md。

* Upstream
> 上游，对于一个branch或者fork来说，源库的主分支即是其它修改信息的源头，被称为upstream，相对的其它branch或fork就被称为downstream了。


# 2.初入github
## 2.1 注册hithub账户&绑定邮箱
> [github官网](https://www.github.com/) <br>这个没什么说的，按照 步骤一步一步就好。邮箱很重要哦，后面经常用到！<br>
![](https://github.com/Allen-Liang/github_for_rookies/raw/master/images/index.png)<br>
> [git官网](https://www.github.com/) <br> git gui&bash客户端下载，选择自己对应的OS下载即可<br>
![](https://github.com/Allen-Liang/github_for_rookies/raw/master/images/git.png)<br>

## 2.2 Windows下Github使用方法 
* git的初始设置
回到桌面，打开git bash，输入以下命令:
> git config --global user.name Your Real Name  <br>
> 填入你的用户名，这个好像可以随意 <br>
> git config --global user.email you@email.address  <br>填入你注册github账户时绑定的email

* 创建SSH密匙
打开git bash，输入以下命令：
> ssh-keygen -C 'your@email.address' -t rsa  <br>
> 然后一路next就好了<br>
> ![](https://github.com/Allen-Liang/github_for_rookies/raw/master/images/key.png) <br>
> 再去查看文件目录（上图代码里面的文件路径），应该就已经有.ssh文件了，这个时候可以复制id_rsa.pub的文件内容到github上。<br>
> 如果打不开pub文件，就用下面的这条命令复制<br>
> clip < ~/.ssh/id_rsa.pub  （如果可以打开pub文件手动复制内容，就不用这行命令了）<br>


* 提交ssh密匙
> 回到github的页面上，在右上方工具栏里找到Account Settings。在这个页面上有一个SSH Public Keys标签，选择Add another public key。Title可以任意填写，Key是刚才生成的ssh public key。在刚才创建密匙的那个目录下找到id_rsa.pub文件，把文件内容拷贝并粘贴到github页面key的空白处。然后Apply，就好了。<br>
> ![](https://github.com/Allen-Liang/github_for_rookies/raw/master/images/ssh.png) <br>
> ![](https://github.com/Allen-Liang/github_for_rookies/raw/master/images/shh2.png) <br>
配置到这里应该可以用了，哈哈哈

* 创建一个远程仓库Repository
> 我们试试在github上面创建一个项目:
> ![](https://github.com/Allen-Liang/github_for_rookies/raw/master/images/1.png) <br>
> ![](https://github.com/Allen-Liang/github_for_rookies/raw/master/images/s1.png) <br>
> 就会有下面的提醒:<br>
> ![](https://github.com/Allen-Liang/github_for_rookies/raw/master/images/s2.png) <br>
 它提供多种方式的创建方法:<br>
* create a new repository on the command line(注意cd到项目路径下)
> ![](https://github.com/Allen-Liang/github_for_rookies/raw/master/images/c.png) <br>
>echo "# github-roam" >> README.md <br>
git init //把这个目录变成Git可以管理的仓库 <br>
git add README.md //文件添加到仓库 <br>
git add . //不但可以跟单一文件，还可以跟通配符，更可以跟目录。一个点就把当前目录下所有未追踪的文件全部add了  <br>
git commit -m "first commit" //把文件提交到仓库 <br>
git remote add origin git@github.com:xxxx/xxxx.git //关联远程仓库 <br>
git push -u origin master //把本地库的所有内容推送到远程库上 <br>

* push an existing repository from the command line
> git remote add origin git@github.com:xxxxxx/xxxx.git <br>
git push -u origin master<br>

* clone一个远程仓库Repository到本地计算机
> 先复制仓库地址<br>
> ![](https://github.com/Allen-Liang/github_for_rookies/raw/master/images/c1.png) <br>
> 启动bash,输入如下命令<br>
> ![](https://github.com/Allen-Liang/github_for_rookies/raw/master/images/c2.png) <br>

* 重新认识github
> ![](https://github.com/Allen-Liang/github_for_rookies/raw/master/images/changku.png) <br> 
> ![](https://github.com/Allen-Liang/github_for_rookies/raw/master/images/haha.png) <br>



# 3.进阶篇

[看大牛的吧_http://github.phodal.com](http://github.phodal.com/) <br>
[看大牛的吧_https://github.com/jasonim/github-guide](https://github.com/jasonim/github-guide/)











