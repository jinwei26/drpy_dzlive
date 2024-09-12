<!--
 * @Author: jinwei26 195569807@qq.com
 * @Date: 2024-09-12 08:48:22
 * @LastEditors: jinwei26 195569807@qq.com
 * @LastEditTime: 2024-09-12 13:21:58
 * @FilePath: \drpy_dzlive\README.md
 * @Description: 这是默认设置,请设置`customMade`, 打开koroFileHeader查看配置 进行设置: https://github.com/OBKoro1/koro1FileHeader/wiki/%E9%85%8D%E7%BD%AE
-->
# drpy_dzlive
来自 https://github.com/jiushizhe/daozhang/tree/main/drpy_dzlive6.21

1、Git初始化及重要配置
   在本地新建个文件夹，命名为HLGithubProject，这个文件夹我叫他“工作文件夹”，这里面会放我们Github上的工程及其文件。
   打开HLGithubProject文件夹，在里面右击，点击Git bash here。
   对Git进行相关的初始化，在打开的git bash窗口中输入：git init
   对Git的user的name进行初始化：git config --global user.name "HLTest"
   对Git的user的email进行初始化：git config --global user.email "HLTest@MeMeDa.com"
   对Git的参数配置进行查询：git config --list

2、Git取消代理  全局命令中输入   
   git config --global --unset http.proxy
   git config --global --unset https.proxy

3、创建SSH密钥 右键 -> Git Bash Here，设置用户名和邮箱
   git config --global user.name "GitHub 用户名"
   git config --global user.email "GitHub 邮箱"
   输入以下命令，然后一路回车
   ssh-keygen -t rsa -C "GitHub 邮箱"
   输入命令 clip < ~/.ssh/id_rsa.pub   可以复制ssh密钥到粘贴板上。
   使用ssh拉取项目 ：git clone git@github.com:jinwei26/drpy_dzlive.git
   
 4、添加密匙：
   进入 [C:\Users\Administrator\.ssh] 目录（要勾选显示“隐藏的项目”），用记事本打开公钥 id_rsa.pub 文件并ctrl+A 复制里面的所有内容。
   2、登陆 GitHub ，进入个人 Settings 页面，不是项目设置页，选择左边栏的 SSH and GPG keys，点击 New SSH key。Title 随便取个名字，粘贴复制的 id_rsa.pub 内容到 Key 中，点击 Add SSH key 完成添加。
5、Github push时  不再支持密码 push  只能将密码换成 your_token 之后才能 push
      在git init，git commit， git add remote 执行之后
      git remote set-url origin  https://<your_token>@github.com/<用户名>/<项目名>.git
6、获取gitHub token
     在github上 点击个人头像 在出来的菜单中 点 setting ->在左边 点 Developer Settings->Tokens(classic) ->右这上边的 Generate new token 下小三角 选择 Generate new token（classic）
      在 Note 中随便填上一个 名字;Expiration中选择时间长一点的 90天；Select scopes下面的选择项全部选上，防止以后出现莫名其秒的问题；-> 选好后点下面的 Generate token -> 得到 token 保存起来避免遗忘
7、对本地项目做一些小操作
   好了，克隆下来这个项目，我们就会对他做一堆操作了，这里只是举个例子，主要是为了说明你利用git进行版本管理的流程：
   git bash窗口下，创建一个test.c文件：touch test.c
   查询状态，输入：git status
   将添加test.c文件的更改添加到暂存区，输入：git add test.c
   将目前版本提交，确认为本地最新版本，输入：git commit -m "add test.c"

6、GitHub Proxy 代理加速： https://ghproxy.liuzhicong.com/

      
    
