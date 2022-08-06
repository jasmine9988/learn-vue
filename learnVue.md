Vue学习
=================



问题
=================


|日期|问题|解答|注意|
|----|----|----|----|
|2022-03-23 |1.DOM是？||在英文模式下写;在控制台可以看到报错;也可以通过控制台修改变量值|
|2022-03-23 |2.双向数据绑定？|||
|2022-03-23 |3.变量后面对应的值 使用的都是单引号？|也可以使用双引号 但都要在英文模式下使用	||
|2022-03-23 |4.控制台通过对象名称.变量名 修改值 生命短?|是的 在内存中修改	||
|2022-03-23 |5.el: '#app'    #代表啥？|https://www.w3school.com.cn/cssref/css_selectors.asp  css选择器中 不同元素的不同选择方式	||
|2022-03-24 |1.v-bind 怎样能一次绑定多个指令  尝试了一下解决  |自己尝试解决|1.举一反三 2.知道了平常页面上hover元素出现tooltip是如何实现的，文本颜色的设置|





每天学到的
=================


2022-08-05
----------------
1. VUE  单文件组件时  如何引入的？

2. 单文件组件内容构成

* template  html标签
> v-model 用input框使用 实现数据双向绑定
> v-on 用于button按钮 绑定函数名
> v-for 同数组使用  列表元素 item 
*  script  js
> 函数 data 定义变量或常量  用于template显示或处理
〉函数methods 定义方法 处理数据
*  style css
3. vm层 即数据连接层   view model

应用由组件构成  组件中由数据和视图  数据和视图如何关联起来 是通过根组件


想改变数据连接层的数据

vm.$data


2022-08-06
--------------------
1.生命周期函数 ：在某一时刻自动执行的函数
> vue自带的嘛？
> 和自己定义的函数的不同 是自动执行？
> 什么应用场景下会用到？

分析代码中是否有事件和声明周期函数
分析代码中是否有数据绑定和组件注入
分析代码中是否有模板 ，没有的话判断是否有innerHtml

2.有哪些
vue实例是否创建完成
beforeCreate()  
Created()
内容是否渲染在页面
beforeMount()
Mounted()

数据是否发生改变
beforeUpdate()
Updated()

销毁实例 vue不服务dom
beforeUnmount()
Unmounted()


![image](https://user-images.githubusercontent.com/102239998/183255520-db27a47e-93ab-4cac-8924-28d0a8f21b96.png)


3.模板中语法
v-html  绑定data下变量中含html标签的数据
v-bind  绑定data中的变量 从而改变标签的属性
v-once 表示只显示一次 后续data中的数据发生改变 不再更新
v-if 
v-show

{{}} 文本插值，花括号中的内容不能显示js语句


2022-03-23
-----------------


1.工具
> HBuilderX,  点击预览按钮， 在内置浏览器下查看vue项目引入

2.Vue.js 2种引入方式
* html文件head下通过<script>引入vue.js

> <script src="vue.js"  type="text/javascript"  chartset="UTF-8"> </script>

* vue单组件，文件名后缀.vue

> vue有不同的构建版本 根据使用 来引版本

3.创建一个应用
> vue.js的应用 由2部分构成，视图和脚本

> 视图中添加变量

> 脚本中为变量进行初始化赋值

> 引入vue.js 就引用了vue的全局变量 ，通过new vue 实例对象获得一个应用。

> 对象要传入2个参数   一个是el  即：element 同id选择器的方式 选中div；一个是data  初始化数据



2022-03-24
-----------------
 
1.v-bind 给元素绑定指令
> 绑定一个指令 v-bind:title="message"

> 绑定多个指令 v-bind="{title:message,color:colorValue}"

2022-03-29 Vue 学习
-----------------
  
1. 数据对象
 
* 声明并初始化

> var data={变量名称：初始值}；

> 多个值时 var data={变量名称：初始值，变量名称2：初始值}；

> 实例中的data下为 data:data
 
* 更新数据的方式

data.变量名称 或者 实例名称.变量名称

2.实例的属性
* 以$符号调用实例下的属性

* 实例名称.$el      等同于 document.getElementById('app')

* 实例名称.$.data.变量名称     等同于   实例名称.变量名称 ，等同于  data.变量名

* 监听数据变化    在数据变化前进行监听

````
 实例名称.$watch('变量名称',function(新值参数,旧值参数){

 console.log(新值参数,参数);

 });
````
 


