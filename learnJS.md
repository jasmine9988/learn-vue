Javascript 学习
=================



问题
=================

|日期|问题|解答|注意|
|----|----|----|----|
|2022-05-24 |1.innerHTML 到底是啥意思 |修改html的内容 ||
|2022-05-25 |1.用反斜杠 对代码折行？ 没看出来效果 |实际是\n||


	






 

JS基本语法
 =================


 2022-05-24
-----------------
 1. 什么是javascript? 作用是啥
 是脚本语言  作用让页面发生动态交互
 2. 如何使用javascript?
  1) 可以直接在html文件中使用  放在html文件下的head或者body
  2) 可以链接外部文件使用    创建js文件夹  添加js文件    在使用的标签内 引入
   ````
       <script src="js/main.js" ></script>
   ````
   3）外链js文件 要注意调用策略 
   当多个js文件  相互独立 不依赖时 使用async
   当多个js文件 中有函数调用时   使用defer   要把依赖的文件 放在最上方
 3. javascript 有浏览器内置的API和外部API,以下是内部的
  1) DOM API  改变html的属性和交互
  2）Canvas/ webgL   画2d/3d图形
  3）地理API

 4. javascript通过以下方式输出数据
  ````
  1) window.alert()
  2) console.log() 向浏览器输出
  3) document.write() 写入html文档
  4) document.geyElementById().innerHTML 写入html元素
  ````

 
  
 2022-05-25  常量/变量/数据类型/变量作用域
-----------------
1. js中名称命名规范
1）区分大小写
2）必须以字母\下划线\美元符号$开头
2. 常量  声明的关键词 const  
          写啥值 常量就赋对应的数值类型
 ````
  		a="test string";
		  b='test char';
		  c=3*5;
		  d=["first","second"];
		  e={"firstName":"wcl","secondName":"ls"};
  ````
3. 变量
3.1 声明变量的方式
第一种 使用关键词 var   可以用来声明局部和全局变量
第二种 使用关键词 let   声明块作用域的局部变量
第三种 变量直接赋值  a=3;  在函数外使用此方式 会产生一个全局变量

3.2 变量赋值
1) 使用let/var声明时 不赋值，那么其值为undefined
如果一个变量未声明 直接访问  会抛引用错误 此变量未定义
undefined 值在布尔类型环境中会被当作 false
数值类型环境中 undefined 值会被转换为 NaN

````
var a;
a + 2;    // 计算为 NaN
````

2) 当你对一个 null 变量求值时，
空值 null 在数值类型环境中会被当作 0 来对待
而布尔类型环境中会被当作 false

````
var n = null;
console.log(n * 32); // 在控制台中会显示 0
````


3.3 作用域
1) 在函数之外声明的变量 是全局变量； 在函数内声明变量添加var关键词 是局部变量，否则是全局变量
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
2）在语句块中用var声明的变量 是全局的；但用let声明 却访问不到

什么是语句块 if语句/循环语句

````
if (true) {
  var x = 5;
}
console.log(x); // 5


if (true) {
  let y = 5;
}
console.log(y); // ReferenceError: y 没有被声明
````

3.4 变量提升





4. 数据类型
4.1 基本数据类型 ：数字 字符串 布尔  null  undefined symbol  （没有字符概念）
4.2  引用数据类型：对象 数组 函数 正则和日期
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
4.3 基本数据类型和引用数据类型的区别
基本数据类型  在变量中存储的是值本身，存在栈中 空间小  读写速度快 操作系统自动分配
引用数据类型  在变量中存储的是地址，栈中存储其内存地址  值存在堆中 存储空间大  读写速度慢  需要程序员分配释放
https://blog.csdn.net/jhfvuyhgui/article/details/123971726

4.4 typeof 判断数据类型  引用数据类型使用typeof只能判断出是object，不能知道具体的对象，
    instanceof 判断左边的变量是否是右边的实例对象
    
````
  a="test string";
  console.log(typeof a);
  
  vars b=new Array();
  console.log(b instanceof Array);


`````

https://blog.csdn.net/qq_41903105/article/details/88372010
 2022-05-26  事件-break
-----------------







JS 函数/类/库
 =================
运算符
 等于和不等于    === ！==         
三元运算符  a?b:c    满足条件a则得到b，否则得出c




JS DOM
=================

2022-06-10   DOM
-----------------
1. 什么是DOM
Document Object Model  文档对象模型
html页面被加载时 浏览器会创建一个dom

2. DOM用来干嘛的
是js操作html元素的接口，js通过dom访问html元素/改变其属性/改变css样式/对页面事件产生反应

3. 如何查找HTML元素
3.1 通过元素的id
getElementById
3.2 通过元素的标签名
getElementByTagName
3.3 通过类名
getElementsByClassName

4. 改变html
1）改变内容  innerHTML
2) 改变属性  attr

5. 改变CSS

6. 对HTML事件作出反应
