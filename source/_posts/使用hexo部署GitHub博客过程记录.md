---
title: 使用hexo部署GitHub博客过程记录
date: 2018-07-12 00:30:17
tags: 
	- miscellaneous
---
关于利用hexo搭建、部署GitHub博客网站，[Hexo官网](https://hexo.io/ "Hexo官网")以及其他教程给出了详细的教程，所以这里只记录我自己的一个过程。

1. 安装[Node.js](http://nodejs.org/en/download/)
2. 安装Hexo并初始化
	```  bash
	npm install -g hexo-cli 
	hexo init  # 在目标目录即博客目录下运行
	npm install hexo-deployer-git --save # 安装hexo-git插件
	```
3. 安装[Git](https://git-scm.com/download/win)，并在[Github](https://github.com/)添加SSH公钥
4. 建立Github个人仓库，仓库名为`$username$.github.io`
5. 链接hexo与GitHub博客仓库
	修改_config.yml文件
	```
deploy:
 	type: git
 	repository: git@github.com:$yourusername$/$yourusername$.github.io.git
 	branch: master

	```
	**注意":"后面需要空格隔开，否则无法识别关键字，导致链接失败！**
6. 绑定域名
	如果有自己的域名可以将其与GitHub博客绑定，从而通过你的域名而不是`$yourusername$.github.io`访问博客
	- 添加A记录，记录值为192.30.252.153
	- 添加CNAME记录，记录值为`$yourusername$.github.io`
	- 在Github博客仓库中的Setting中修改Custom domain为你的域名
	- 进入本地博客目录下的source，创建文本文件CNAME，无文件后缀`.txt`,并把你的域名写入文本文件中
7. 更换主题
	- 在hexo的[Themes](https://hexo.io/themes/)中挑选喜欢的主题，并clone到本地目录的theme目录下
	- 将_config.yml中的`theme`关键字的值改为新主题的文件夹名称
8. 部署到GitHub博客上
	```
	hexo g # 生成静态网页文件
	hexo d # 部署到Github
	```
	以上代码可以等价于`hexo d -g`或`hexo g -d` 在每一次修改后都可以执行这些指令，同步到GitHub博客上
9. 其他常用命令
	```
	hexo new [layout] <title> # 在本地/sourece/_post目录下生成md文件，该文件对应一篇博客文章页面
	hexo s # 启动服务器。默认情况下，访问网址为： http://localhost:4000/
	```
	更多命令与使用可查看[官网教程](https://hexo.io/zh-cn/docs/)
