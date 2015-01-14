# node-express-handlebars
自己学习使用node+express+handlebars框架搭建本地环境

1.首先安装node（http://nodejs.org/）官方方正下载下来，安装即可

2.使用node自带的npm 安装相关环境（目前先安装express）
  
	键入命令：npm install express -g 回车等待安装express........
	
3.使用express创建项目

	键入命令：express -e node-express-handlebars

4.选运行本地环境

	键入命令：npm install (先安装依赖包)
	
	键入命令：npm start  (开启服务)
	
5.在浏览器地址栏中输入：http://localhost:3000/ 即可看到效果

6.由于express创建的项目默认为ejs模板，我想改为使用handlebars.js模板，先安装express-handlebars

	在项目根目录下：
	
	键入命令：npm install express-handlebars
	
7.修改vides目录下的index.ejs ->index.html,  error.ejs ->error.html (把index.html里面的<%  %>改为{{  }})

8.打开app.js

	添加 var exphbs  = require('express-handlebars');
	
	修改
	app.set('view engine', 'ejs');
	为以下 >>
	app.engine('.html', exphbs({extname: '.html'}));
	app.set('view engine', 'html');

9.然后刷新浏览器，大功告成！！！！


	

