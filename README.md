<!--
 * @Author: jinwei26 195569807@qq.com
 * @Date: 2024-09-12 08:48:22
 * @LastEditors: jinwei26 195569807@qq.com
 * @LastEditTime: 2024-09-12 09:18:27
 * @FilePath: \drpy_dzlive\README.md
 * @Description: 这是默认设置,请设置`customMade`, 打开koroFileHeader查看配置 进行设置: https://github.com/OBKoro1/koro1FileHeader/wiki/%E9%85%8D%E7%BD%AE
-->
# drpy_dzlive
来自 https://github.com/jiushizhe/daozhang/tree/main/drpy_dzlive6.21

1、Git取消代理  全局命令中输入   
   git config --global --unset http.proxy
   git config --global --unset https.proxy

2、创建SSH密钥 右键 -> Git Bash Here，设置用户名和邮箱
   git config --global user.name "GitHub 用户名"
   git config --global user.email "GitHub 邮箱"
   输入以下命令，然后一路回车
   ssh-keygen -t rsa -C "GitHub 邮箱"
   
   添加密匙：
   1、进入 [C:\Users\Administrator\.ssh] 目录（要勾选显示“隐藏的项目”），用记事本打开公钥 id_rsa.pub 文件并ctrl+A 复制里面的所有内容。
   2、登陆 GitHub ，进入 Settings 页面，选择左边栏的 Deploy keys，点击 New SSH key。Title 随便取个名字，粘贴复制的 id_rsa.pub 内容到 Key 中，点击 Add SSH key 完成添加。