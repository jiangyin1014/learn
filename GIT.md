readme
1.从官网下载安装Git
2.菜单--Git--Git Bash
3.初始设置
  git congfig --global user.name "JYY-PC"
  git congfig --global user.email "787280034@qq.com"
4.登录Github,settings--SSH and GPG keys--New SSH key，title随便起个名字，SSH key从本地 id_rsa.pub 复制粘贴，Add SSH key
5.生成SSH密钥
  ssh-keygen -t rsa -C "787280034@qq.com"
  直接按回车即可
  在PC的C盘/用户/JYY/目录下会生成 .ssh文件夹，里面的id_rsa是密钥，id_rsa.pub是公钥，我们需要的是公钥，将id_rsa.pub的内容拷贝至Github的SSH key处
6.cd F:/Code/
  mkdir work
  cd work
7.初始化仓库
  git init
  修改文件
  vim readme.md
  将文件添加到仓库
  git add readme.md
  将文件提交到仓库
  git commit -m "add readme.md"
  关联远程仓库
  git remote add origin https://github.com/jiangyin1014/learn.git
  推送至远程仓库
  git push -u origin master
