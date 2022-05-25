Javascript 学习
=================



问题
=================

|日期|问题|解答|注意|
|----|----|----|----|
|2022-05-24 |1.innerHTML 到底是啥意思 | ||
|2022-05-25 |1.用反斜杠 对代码折行？ 没看出来效果 | ||


	







每天学到的
 
 =================
 


 2022-05-24
-----------------
 1. 什么是javascript? 作用是啥
 是脚本语言  作用让页面发生动态交互
 2. 如何使用javascript?
  1) 可以直接在html文件中使用  放在html文件下的head或者body
  2) 可以链接外部文件使用    创建js文件夹  添加js文件    在使用的标签内 引入
   ````
       <script src="js/main.js"></script>
   ````
 3. javascript 有内置的API和外部API,以下是内部的
  1) DOM API  改变html的属性和交互
  2）Canvas/ webgL   画2d/3d图形
  3）地理API

 4.javascript通过以下方式输出数据
  ````
  1) window.alert()
  2) console.log() 向浏览器输出
  3) document.write() 写入html文档
  4) document.geyElementById().innerHTML 写入html元素
  ````
	
  5. 常量的定义   写啥值 常量就赋对应的数值类型
  
  ````
  		a="test string";
		  b='test char';
		  c=3*5;
		  d=["first","second"];
		  e={"firstName":"wcl","secondName":"ls"};
  ````
  
  6. 变量定义    关键词var
  
  
  
  
  
  
 2022-05-25
-----------------
1.区分大小写
2.代码逐行执行
