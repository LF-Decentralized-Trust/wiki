1. [Technical Working Group China](index.html)
2. [Technical Working Group China](Technical-Working-Group-China_22151170.html)
3. [i18n and Education](i18n-and-Education_22151244.html)

# Technical Working Group China : Getting Started

Created by Yang Cheng, last modified on Jul 25, 2020

## **文档翻译要求**

文档翻译工作由大家协作完成，每个人的习惯有所不同，为了使翻译内容整齐规范，建议大家翻译时参照本规范翻译文档内容和整理文档格式。具体内容如下：

- 翻译前请先阅读[**《术语表》**](https://hyperledger-fabric-cn.readthedocs.io/zh/latest/glossary.html)，文中术语尽量按照术语表翻译，以免产生歧义；对于一些专有名词，容易引起歧义的单词，可以保留原单词不做翻译。
- 文档语句采用逐字逐句**“正翻”**的方法，不可自由发挥，确保翻译的严谨性，但是为了保证语义通顺，请合理地调整语序，我们知道英文的语言习惯和中文是不一样的；
- 在中文语句中出现的英文单词，应在**英文单词前后各空一格**，使文档保持美观。除非和英文单词相邻的是标点符号，这种情况可不加空格。
- 翻译语句的标点符号请**使用中文标点**，避免中英文标点混用的情况。提示：英文中没有顿号“、”，所以都使用逗号“,”表示停顿，在中文翻译中请使用“、”替换。
- 对于文中的引用、代码块、超链接，其内容可以保持原文，**不强制要求翻译**。
- 原文语句中的**加粗、重点、斜体等标记**，在翻译时也应该同样标记出来。

## **翻译流程**

### 1、前期工作

1\) 注册 Github 账号，将[官方仓库（https://github.com/hyperledger/fabric-docs-i18n）](https://github.com/hyperledger/fabric-docs-i18n) Fork 到自己的仓库。

2\) 下载 git，[https://www.git-scm.com/download/](https://www.git-scm.com/download/)，安装运行 gitbash。

3\) 设置 SSH：

a) 打开 git bash，输入命令：

ssh-keygen

![](attachments/22151280/22151320.png?height=250)

cat .ssh/id

![](attachments/22151280/22151321.png?height=70)

git config --global user.name "自己的名字或者GitHub账户名字"  
git config --global user.email 自己GitHub的认证邮箱账户

b) 打开 github 网页，网页右上角 settings – SSH and GPG keys – New SSH key。将 cat 命令打印的内容拷贝粘贴到 New SSH key 里面。

![](attachments/22151280/22151322.png?height=234)

4) 克隆仓库并更改 branch

a) 打开 github，找到自己 fork 的仓库，clone with SSH，复制

![](attachments/22151280/22152310.png?height=400)

b) 打开 git bash，粘贴复制的内容  
git clone git@github.com:自己的/fabric-docs-i18n.git

cd fabric-docs-i18n

c) 切换 branch（从master到 release-2.2 或者其他需要翻译的分支）  
git branch –a  
git checkout -b  release-2.2

![](attachments/22151280/22152313.png?height=190)

### 2、认领任务

1.**查看 [issue 列表](https://github.com/hyperledger-labs/fabric-docs-cn/issues)**，根据当前任务的进度选择你要认领的任务。

2.**添加评论**表明你要领取该翻译任务，然后等待管理员将任务分配给你。如下图：

![](attachments/22151280/22152001.png?width=500)

3.如果issue中没有列出你要翻译的内容，在确保该内容没有人翻译的情况下，**添加新issue**，并添加评论表明你要认领该任务。

4.管理员将任务分配后，即可开始**翻译**。

**注意：任务自被分配之日起两周未完成的可以被其他人重新认领。**

### 3、翻译上传

1)  编辑中文版（位置目录：fabric-docs-cn/docs/source）

选择合适的 md/rst 格式文件编辑器（ [typora](https://www.typora.io/)，VSCode，Atom，vim等），直接编辑对应文件。（如有 IDE 则可直接编辑，rst 可在 [http://rst.ninjs.org/](http://rst.ninjs.org/) 上审阅）  
注意格式：斜体、粗体、超链接、注释……

2) 提交更改、signoff 及合并

cd fabric-docs-cn  
查看文件变化：git diff （Ctrl+c退出）  
git add docs/source/文件名  
Signoff提交：git commit **-s** m "这里用英文写本次提交翻译了什么"   **（注意加 “ -s” 参数）**  
git push

![](attachments/22151280/22151327.png?height=250)

3)  打开Github：Pull request – New pull request，比较上传，申请合并（填写描述）

![](attachments/22151280/22151328.png?height=126)

## **Fabric Documents Translate Workflow**

**1. Prepare Documents Repository**

1\) Login Github and fork [https://github.com/hyperledger-labs/fabric-docs-cn](https://github.com/hyperledger-labs/fabric-docs-cn)

2\) Install git, more details see [https://git-scm.com/downloads](https://git-scm.com/downloads.)

3\) Generate SSH key and it to your Github account, more details see [https://help.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh](https://help.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh)

4\) Clone the documents repository to your local use commond “*git clone repo-url*“, and checkout branch you want to use, like “*git checkout -b release-2.2*” it will change to branch release-2.2 which is Chinese translation branch.

**2. Claim Tasks**

1\) Check the issue list [https://github.com/hyperledger/fabric-docs-i18n/issues](https://github.com/hyperledger/fabric-docs-i18n/issues)

2\) Add a comment under the issue you want to claim, then wait for assigning by administrator. Like this:

 ![](attachments/22151280/22152001.png?height=400)

3\) If the list not contains the document you want to translate, make sure nobody has translated it, and then you can add an new issue,and leave a comment, then wait for assigning

4\) Translate the documents after the administrator assigned it to you**NOTE**: If the issue is assigned more than two weeks, but not finished,anybody else can claim the issue again.

**3. Upload Your Translations**

1\) Translate the documents with property editor,like Typora, VSCode, Atom, Vim. The source files are in fabric-docs-cn/docs/source directory

2\) Commit and push your translation with signoff. The commonds are like this:

- *git commit -s -m “your message”*
- *git push*

3\) Create a new Pull Reques in repository [https://github.com/hyperledger/fabric-docs-i18n/issues](https://github.com/hyperledger/fabric-docs-i18n/issues)[,](https://github.com/hyperledger-labs/fabric-docs-cn,)you can find it by chose “Pull request – New pull request”, then compare changes and create a PR with a message for want you have done.Like this:

![](attachments/22151280/22152066.png?width=611)

4\) Waiting for merge by administrator

## Attachments:

![](images/icons/bullet_blue.gif) [image2019-2-27\_9-26-49.png](attachments/22151280/22151320.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2019-2-27\_9-26-55.png](attachments/22151280/22151321.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2019-2-27\_9-27-46.png](attachments/22151280/22151322.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2019-2-27\_9-28-9.png](attachments/22151280/22151323.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2019-2-27\_9-28-20.png](attachments/22151280/22151324.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2019-2-27\_9-28-30.png](attachments/22151280/22151325.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2019-2-27\_9-28-42.png](attachments/22151280/22151326.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2019-2-27\_9-38-16.png](attachments/22151280/22151327.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2019-2-27\_9-38-37.png](attachments/22151280/22151328.png) (image/png)  
![](images/icons/bullet_blue.gif) [assign.png](attachments/22151280/22151707.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2019-4-26\_13-34-59.png](attachments/22151280/22151720.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2019-4-26\_13-46-14.png](attachments/22151280/22151721.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2019-4-26\_13-47-40.png](attachments/22151280/22151722.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2019-4-26\_13-44-4.png](attachments/22151280/22151723.png) (image/png)  
![](images/icons/bullet_blue.gif) [Screenshot from 2020-04-04 14-29-03.png](attachments/22151280/22151999.png) (image/png)  
![](images/icons/bullet_blue.gif) [Screenshot from 2020-04-04 14-46-33.png](attachments/22151280/22152001.png) (image/png)  
![](images/icons/bullet_blue.gif) [pr.png](attachments/22151280/22152066.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2020-7-25\_22-15-53.png](attachments/22151280/22152309.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2020-7-25\_22-16-46.png](attachments/22151280/22152310.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2020-7-25\_22-17-26.png](attachments/22151280/22152311.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2020-7-25\_22-27-41.png](attachments/22151280/22152313.png) (image/png)

Document generated by Confluence on Nov 26, 2024 15:10

[Atlassian](http://www.atlassian.com/)
