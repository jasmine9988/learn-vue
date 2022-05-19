# learn-Flex



https://design.zhihuiya.com/storybook/next/?path=/docs/css-flex--example-1

![lQLPDhtmKPD8xFnNAdPNBLCwmeQdbIJTwlUCeA1RpUD-AA_1200_467](https://user-images.githubusercontent.com/102239998/167246579-1d098fed-1b59-4a06-8a6b-3b9e73dc9e6b.png)










https://blog.csdn.net/CS13477062349/article/details/79269732


2022-05-11
-----------------------------

理解
有了flex   
1）不需要每个元素都设置position/margin
2）可以复用同一样式
3）盒子模型
主轴即X轴  交叉轴即Y轴
主轴的起点 flex-start  
主轴的终点 flex-end

样式都要先设置display:flex

属性  
1) flex-direction   盒子内容的方向
值   row    盒子中的元素 按照主轴的方向线上
     row-reverse 盒子中的元素按照主轴的反方向显示  元素整个调过来
     cloumn （交叉轴的方向即垂直显示） 
     cloumn-reverse（交叉轴的反方向）
     
    
2）flex-wrap
使用此属性的前提条件   
第一：盒子定义了宽度，盒子内的元素定义了宽度    第二：盒子内元素的宽度总和 大于 盒子的宽度
值 -wrap 盒子内容元素换行显示
   -nowrap 盒子内元素不换行  溢出显示










2) justify-content  水平对齐        >>justify的翻译 是每行排齐
值   center (居中)
     flex-start (显示在主轴起点)
     flex-end （显示在主轴重点）
     space-around （元素 中间间距是2边间距的和）
     space-between（元素中间有间距  两边无间距）
4) align-content
多个轴线 才可用
5) align-items  垂直对齐 >> align的翻译 使每列排齐
值  center （以Y轴居中）
    flex-start（垂直顶部）
    flext-end（垂直底部）
    stretch（沿上下方向垂直伸缩）
