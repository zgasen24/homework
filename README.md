# Git 学习笔记
  
## 一、资料来源与相关连接    
主要在B站上学习，有问题问豆包解决了  
https://www.bilibili.com/video/BV1u94y1n73L/?spm_id_from=333.337.search-card.all.click&vd_source=9a3a7ba5c9b1877ce993a128bb2ab1bf  
https://www.bilibili.com/video/BV1d6XVYqEuy/?spm_id_from=333.337.search-card.all.click&vd_source=9a3a7ba5c9b1877ce993a128bb2ab1bf  

## 二、实践过程
在官网下载安装  
初次使用右键，在下拉菜单选择Open Git Bash Here  
进入后参照视频进行了常用命令的学习，使用流程为修改代码->存到暂存区（add）->提交到本地仓库（commit）->远程连接Github仓库（remote）->把代码推到Github（push）
每次提交时已添加备注（git commit -m"  "），至于代码内容，只时随便编了一小段代码供自己学习而已
## 三、问题及方法
1.关于git diff命令的相关操作和HEAD的相关说明刚开始并不清晰，后续问豆包解决，也一同附在了下面  
2.远程连接遇到的问题，通过视频了解到会有多种连接方式，我这个仓库采用HTTP+令牌的方式（有效期为一个月）  
## 四、学习心得
Git与Linux是同一个人写出来的，所以一开始上手就感觉二者操作很相似；再谈Git的实用性，作为一个代码版本管理的软件，比自己手动备份要简单便捷不少，像Github这样远程仓库酷似云端的方式，让多人协同创作一段代码也不会乱套，确实是一件利器
## 五、一些常用命令  
在项目文件夹创建本地仓库  
git init  

设置全局用户名（仅第一次配置）  
git config --global user.name "你的名字"  
  
设置全局邮箱（仅第一次配置）  
git config --global user.email "你的邮箱"  
  
查看当前配置  
git config --list  
  
添加单个文件到暂存区  
git add 文件名  
  
添加所有修改到暂存区（最常用）  
git add .  
  
提交到本地仓库（必须写备注）  
git commit -m "备注内容"  
  
查看完整提交日志  
git log  
  
查看提交+文件修改统计  
git log --stat  
  
查看简洁版日志  
git log --oneline  
  
对比版本差异  
git diff [commit id]   

强制回退到指定版本（慎用！会覆盖本地代码）  
git reset --hard [commit id]  
  
回退到上一版本  
git reset --hard HEAD^  
  
回退到上两个版本  
git reset --hard HEAD^^  
  
恢复文件到上次提交状态  
git checkout -- 文件名  
git restore 文件名  
  
从暂存区撤回到工作区  
git reset HEAD 文件名  
git restore --staged 文件名    
  
绑定远程仓库  
git remote add origin 仓库地址  
  
查看远程仓库信息  
git remote -v  
  
第一次推送到远程（绑定上游）  
git push -u origin main  
  
后续常规推送  
git push  
  
拉取远程最新代码  
git pull  
  
HEAD：当前最新版本  
HEAD^：上一个版本  
HEAD^^：上两个版本  
commit id：版本号（可通过 git log 查看）  
