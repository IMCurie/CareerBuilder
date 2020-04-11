### 前端练习一的总结

1、透明背景

> background-color: transparent;

2、背景遮罩

> background-color: black;
> opacity: 0.4;

​	相当于

>  background-color: rgba(255, 255, 255, 0.4);  0.4就是设置透明度

3、元素脱离文档流如何不覆盖下面的元素

> 在脱离文档流元素的下面增加个div

4、元素浮动如何居中

> 在该浮动元素外面嵌套个div并设置 margin: auto;

5、fixed

> 也会脱离文档流，同样可以设置z-index(参数大的在上面)

6、清楚浮动（清除浮动主要是为了解决，父元素因为子级元素浮动引起的内部高度为0的问题）

> 额外标签法（在最后一个浮动标签后，新加一个标签，给其设置clear：both；）
>
> clear：both：本质就是闭合浮动， 就是让父盒子闭合出口和入口，不让子盒子出来

> 父级添加overflow属性（父元素添加overflow:hidden）

> 使用after伪元素清除浮动（推荐使用）
>
>  .clearfix:after{/*伪元素是行内元素 正常浏览器清除浮动方法*/
>         content: "";
>         display: block;
>         height: 0;
>         clear:both;
>         visibility: hidden;
>
> }

7、内联元素

> 内联元素(inline)不会独占一行，相邻的内联元素会排在同一行。其宽度随内容的变化而变化
>
> 内联元素不可以设置宽高 
>
> 内联元素可以设置margin，padding，但只在水平方向有效
>
> 实现边上带小三角的div提示框

9、垂直对居中齐

> .center {    
>
> ​	padding: 70px 0; 
>
> ​	border: 3px solid green;
>
> }
>
> 如果是一行东西，可以
>
> 可以设置div高度和行高一样

10、实现边框带小三角的div提示框

> div{
>     margin: 0px;
>     border-width: 15px;
>     border-style: solid;
>     border-color: transparent #07cbc9 transparent transparent;
>     padding: 0px;
>     width: 0px;
>     height: 0px;
> }