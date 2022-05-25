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
  
  
  
  
  
  
 2022-05-25  变量/常量/数据类型/变量作用域
-----------------
1.区分大小写
2.代码逐行执行
3.变量
1）通过typeof 可以得到变量对应的数据类型
````
  var cars="test string";
  console.log(typeof cars);

````
2）作用域
````

        <p id="paramGlobal">全局变量</p>
	<p id="paramRange">局部变量</p>
          <script>
		  function testFunction(a,b){
			  var limitparam="test limit param";//函数内使用var声明了 变成局部变量 外部不可使用
			  globalparam="test global param";//函数内未使用var声明   即是全局变量 外部可使用
			  return a*b;
		  }
		  
		  document.getElementById("paramGlobal").innerHTML=globalparam;//全局变量 可调用
		  document.getElementById("paramRange").innerHTML=limitparam;//局部变量不可调用
         <\script>
````

4.数据类型
1）bool   值为ture  false
2）数组   以下三种方式
````
第一种
var array1=new array();
array1[0]="test";
array2[1]="test2";

第二种
 var array2=["test1","test2"];
 
第三种
 var array2=new Array("test1","test2");

````
3) 对象 
````
<p id="test">test</p>
<script>
  var duixiang={age:1,name:wcl};// key:value  花括号
  
  var duixiang2={fullattr:function(){
                          return duixiang.age+duixiang.name;
			  }
		}
		
 document.getElementById("test").innerHTML=duixiang2.fullattr;//返回对象定义的方法 作为字符串
		  
 document.getElementById("test").innerHTML=duixiang2.fullattr();//返回对象方法里的内容		
</script>		
			  
````
