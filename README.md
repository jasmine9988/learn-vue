# learn-vue



|日期|问题|解答|注意|
|----|----|----|----|
|2022-03-23|DOM是？||在英文模式下写;在控制台可以看到报错;也可以通过控制台修改变量值|



2022-03-23
1.工具
HBuilderX,  点击预览按钮， 在内置浏览器下查看vue项目引入

2. Vue.js 2种引入方式
1) html文件head下通过<script>引入vue.js

<script src="vue.js"  type="text/javascript"  chartset="UTF-8"> </script>

2）vue单组件，文件名后缀.vue

vue有不同的构建版本 根据使用 来引版本

3.创建一个应用
vue.js的应用 由2部分构成，视图和脚本

视图中添加变量

脚本中为变量进行初始化赋值

引入vue.js 就引用了vue的全局变量 ，通过new vue 实例对象获得一个应用。

对象要传入2个参数   一个是el  即：element 同id选择器的方式 选中div；一个是data  初始化数据



2022-03-24
1.v-bind 给元素绑定指令
绑定一个指令 v-bind:title="message"

绑定多个指令 v-bind="{title:message,color:colorValue}"

2022-03-29
1. 数据对象
1）声明并初始化

var data={变量名称：初始值}；

多个值时 var data={变量名称：初始值，变量名称2：初始值}；

实例中的data下为 data:data
2）更新数据的方式

data.变量名称 或者 实例名称.变量名称

2.实例的属性
以$符号调用实例下的属性

1）实例名称.$el      等同于 document.getElementById('app')

2)  实例名称.$.data.变量名称     等同于   实例名称.变量名称 ，等同于  data.变量名

3）监听数据变化    在数据变化前进行监听

实例名称.$watch('变量名称',function(新值参数,旧值参数){

console.log(新值参数,参数);

});
