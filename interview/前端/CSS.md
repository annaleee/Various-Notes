# CSS常问面经

## 书

1. CSS权威指南

## link type of CSS

   1. external style sheet: `<link rel="stylesheet" type="text/css" href="mystyle.css">`
   2. internal style sheet:

        ```CSS
        <head>
        <style>
            hr {color:sienna;}
            p {margin-left:20px;}
            body {background-image:url("images/back40.gif");}
        </style>
        </head>
        ```

   3. inline style sheet: `<p style="color:sienna;margin-left:20px">这是一个段落。</p>`

### style优先级

inline style > internal style sheet > external style sheet.  

## what is position

1. static: default value。 浏览器会按照源码的顺序，决定每个元素的位置。(normal flow) 元素与元素之间不产生重叠，这个就是元素的默认位置。此时top, bottom, left, right无效。
2. relative: 相对于默认位置进行偏移（static时的位置），要搭配top, bottom, left, right来一起使用。
3. fixed: 相对于浏览器窗口，如果搭配top, bottom, left, right这四个属性使用，表示元素的初始位置是基于视图计算的，否则初始位置就是元素的默认位置。
4. absolute: 相对于上级元素进行定位，父元素不能是static定位，如果父元素是static，定位基点就会变成整个html网页的根元素，另外，也必须配合top, bottom, left, right来一起使用
5. sticky: sticky生效的前提：必须搭配top, bottom, left, right一起使用，不能省略，不然等同于relative定位。当页面滚动，父元素部分不可见且达到门槛值，就自动切换为fixed，当父元素全部不可见，就自动切换为relative

## flex

flexible box，元素称为flex-container,有main axis和cross axis，根据这两条主轴来排列每一个元素，可以称为一维布局

## grid是什么

把网页划分成一个个网格，二维布局，inline-grid就是这个元素内部是grid，整体是inline的。在container里设定grid-template-columns 和grid-template-rows.

1. justify-self: 单元格内容的水平位置
2. align-self: 设置单元格的垂直位置
3. stretch: 拉伸，占满单元格的整个宽度
4. place-self: align-self和justify-self的结合

## display

1. none: 不占据空间，无法显示
2. inline: 高度宽度无效，text-align无效，设置了line-height会让inline元素居中
3. block: 如果不指定宽高，默认会继承父元素的宽度，并且独占一行
4. inline-block: block的宽高特性又有inline的同行特性
5. flex: 子元素的float，clear，vertical-align失效

## float

1. float以后，保证自己的顶部和上一个元素的底部对齐
2. 向左或者向右浮动，直到自己的边界紧贴着包含块或者其他浮动元素的边界为止
3. 定位元素会层叠在浮动元素上面
4. 不能超出包含块
5. 浮动元素不能层叠
6. 浮动元素会将inline元素推出
7. 浮动只能左右浮动，不能超出本行的高度

## clear

1. none: 允许浮动元素
2. left: 如果当前元素的左侧有浮动元素，那么就强制该元素另起一行
3. both: 左右都不行

## text-align: justify

1. 文字两侧对齐，对最后一行无效

## how to center en element

1. center block: margin:auto
2. center the text: text-align:center
3. use position: left and right to

## CSS reset and CSS normalize

每一个浏览器的css默认值都不一样，为了保证在所有的浏览器中css得到一个稳定的呈现，可以利用css重置把css全部归零  
css normalize则是  

1. 保护有用的浏览器默认样式而不是完全去掉它们
2. 一般化的样式：为大部分HTML元素提供
3. 修复浏览器自身的bug并保证各浏览器的一致性
4. 优化CSS可用性：用一些小技巧
5. 解释代码：用注释和详细的文档来

官方文档：[CSS normalize]<http://necolas.github.io/normalize.css/>

## box-sizing

这个属性意思是如何定义box的总高度和总宽度，到底要不要算border padding

## BEM

block，element，modifier 合称为bem  
[官方文档](https://getbem.com/introduction/)
是一个对于class的官方命名法，让代码更规范，block__element--modifier  
[参考文档](https://www.infoq.cn/article/vfnfwdle0zmga9psvbug)

## css-module

## scss/sass

[教程](https://juejin.cn/post/7046323233427030053)

## card element

一种命名方法 card-element