HTML 学习
=================



问题
=================

|日期|问题|解答|注意|
|----|----|----|----|
|2022-04-01 |1. html中 div p h3的关系 | 1.百度查询 学多了自然知道  每个公司规范不同https://q.cnblogs.com/q/82362/ ||
|2022-04-01 |1. html中 不同元素的不同属性 发现并不是有些属性 某些元素没有 为什么 |||
|2022-04-02 |1. html中 一个目录下不能出现多个html文件？ 跳转链接拼接到上一个地址后面了 ![image](https://user-images.githubusercontent.com/102239998/161368475-e888dc81-4994-43f9-acf1-fff73e80bd30.png) |能出现  和多个html无关  因为未定义http协议||
|2022-04-02 |2.  <basefont> 标签不支持使用了？||
|2022-04-21 |1.  拿到一个页面 要规划组成  每个标签要定义属性 不能一骨碌全写||
	







每天学到的
 
 =================
 
 空标签总结
 ------------------
 ````
 <br/>
 ````
 | 空标签-无结束标签|描述|
 |----|----|
 | br|换行|
 |img|插入图片|
 
 
 
 


 2022-04-01 
-----------------
 1. span 行内元素
 2. div 块级元素 p 段落级
 3.  插入的图片放到img文件夹下
  ````
 <img src="img/test.png"/> 
  ````

 4. 空白内容 
 
  ````
    &nbsp;

  ````

 2022-04-02
-----------------
1.字体加粗
````
<b>加粗</b>
````
2.<base> 标签为页面上的所有链接规定默认地址或默认目标。

通常情况下，浏览器会从当前文档的 URL 中提取相应的元素来填写相对 URL 中的空白。

使用 <base> 标签可以改变这一点。浏览器随后将不再使用当前文档的 URL，而使用指定的基本 URL 来解析所有的相对 URL。这其中包括 <a>、<img>、<link>、<form> 标签中的 URL。

 需要操作下
 

  
 3. 
 ````
 <blockquote> 与 </blockquote>   块引用   支持内容缩进  <q>和</q> 短内容引用
 ````

 4. 
 ````
    canvas.getContext('2d')  为画布提供环境   暂只支持2D的图
    canvas  画矢量图 拥有基于javascript的API
  ````
 
 5. button
 6. 表单
 
 1）fieldset 相关元素分组
 ````
 <form>
  <fieldset>
    <legend>health information</legend>
    height: <input type="text" />
    weight: <input type="text" />
  </fieldset>
</form>

 ````
![image](https://user-images.githubusercontent.com/102239998/161372074-aba77a21-58ed-4e0e-970a-3a59b888e9f5.png)

 2) input
 ````
 <!--表单-->
		<form>
			<div>
			花花：
			<input type="checkbox" checked="checked" />
			<br/>
			小草:
			<input type="checkbox" />	
			</div>
		</form>
			<div>
				男性：
				<input type="radio" checked="checked" />
				女性：
				<input type="radio" />
				<br/>
			</div>

			用户名：
			<input type="text" maxlength="20" value="wcl" />
			密码：
			<input type="password"/>
			<br/>
			<input type="button" value="submit" />
			
			<form>
				<select name="cars" he>
					<option value="value1">nissan</option>
					<option value="value1" selected="selected">benzi</option>
				</select>
			</form>
		
		 <br/>
		  <textarea rows="10"  cols="10"> textarea</textarea>
 ````

 
 ![image](https://user-images.githubusercontent.com/102239998/161374182-2f7d2197-3c4d-49c2-9ca0-17124e64baa0.png)

 7.列表
1) ol type属性支持的值：A/a/I/i/1
2) ul type属性支持的值：disc/circle/square
	
![image](https://user-images.githubusercontent.com/102239998/161374612-18bad480-b5e3-46a0-b1f8-6fd3ad99d401.png)	
	
 ````
		<h4>一个无序列表：</h4>
		<ol type="1">
			<li>apple</li>
			<li>pear</li>
		</ol>
		
		<h4>一个有序列表：</h4>
		<ul type="circle">
			<li>water</ol>
			<li>juice</ol>
		</ul>	
 ````
	
8.元素指定样式 
	
	
1）链接外部样式表 head 标签下定义
	
	````
	<head>	
	<link rel="stylesheet" type="text/css" href="./css/diagnose.css" />
	</head>		
        ````
2) 链接内部样式 head 标签下定义
	
````
<head>	
<style type="text/css">
       h2 {
	color:cornflowerblue;
	}
</style>
</head>	
````
3）标签 单独定义样式
	
````
	<div style="padding-top: 1px; padding-bottom: 1px;"> test </div>
````	
	
	
	
 2022-06-15  HTML 事件属性
-----------------
1. button   onclick()  ondblclick()
2. 表单input   onfucs()
3. 鼠标点击事件
	

	

