# CSS
* 在前端开发中，对于外观控制一般用CSS来实现，而不是使用标签来实现，这更加符合结构与样式分离的原则，提高可读性和可维护性。
### 一、CSS引入方式
1、外部样式表 `<link rel="stylesheet" type="text/css" href="文件路径" />` <br>
2、内部样式表 `<style type="text/css"></style>`
### 二、CSS选择器
1、元素选择器 <br>
2、id选择器 <br>
3、class选择器 <br>
4、后代选择器：选择元素内部中所有的某一种元素，包括子元素和`其他后代元素` ，eg: `#father1 div {...}` 父元素和后代元素中间用空格隔开 <br>
5、群组选择器：两个选择器之间必须要用英文逗号（,）隔开
### 三、字体样式
1、font-family 字体类型 <br>
如果字体类型只有一个英文单词，则不需要加上双引号；如果字体类型是多个英文单词或者中文的，则需要加上双引号。 <br>
2、font-size 字体大小 <br>
3、font-weight	字体粗细 <br>
取值：`normal、lighter、bold、bolder `<br>
4、font-style 字体风格 <br>
5、color	字体颜色 <br>
英文或者16进制颜色值（#000000 黑色；#FFFFFF 白色）
### 四、文本样式
1、text-indent	首行缩进 <br> 
text-indent值应该是font-size值的2倍 <br>
2、text-align 水平对齐 <br>
取值：`left	左对齐（默认值）；center	居中对齐；right 右对齐` <br>
3、text-decoration 文本修饰 <br>
取值：`none（默认值）；underline 下划线；line-through 中划线；overline 顶划线` <br>
在实际开发中，通常会使用text-decoration:none; 去除a元素的下划线 <br>
4、text-transform 大小写转换	<br>
取值：`none （默认值）；uppercase 转换为大写；lowercase 转换为小写；capitalize 只将每个英文单词首字母转换为大写` <br>
5、line-height	行高 <br>
6、letter-spacing 字母间距 <br>
7、word-spacing 词间距 <br>
### 五、边框样式
    border: border-width border-style border-color;
    eg:
    border: 1px solid red; /*样式：none；dashed 虚线；solid 实线 */
局部样式：border-top、border-bottom、border-left、border-right <br>
删除某个边，如border-bottom: 0px; 、 border-bottom: 0; 和border-bottom: none ;是等价的
### 六、列表样式
1、列表项符号 list-style-type <br>
list-style-type属性是针对ol或者ul元素的，开发中常用`list-style-type: none;` <br>
2、列表项图片 list-style-image <br>
定义列表项图片，也就是使用图片来代替列表项符号

    list-style-image: url(图片路径);
注：在实际开发中，一般情况下都不会用list-style-image属性来实现，而是使用更为高级的iconfont图标技术
### 七、表格样式
1、表格标题位置 caption-side <br>
取值：`top（默认）、bottom` <br>
2、表格边框合并 border-collapse <br>
使用border-collapse属性来去除单元格之间的空隙，也就是将两条边框合并为一条。<br>
取值：`separate 边框分开，有空隙（默认值）；collapse	边框合并，无空隙` <br>
3、表格边框间距 border-spacing <br>
* 以上属性都在table元素中定义
### 八、图片样式
1、图片对齐 <br>
水平对齐：text-align 取值：`left、center、right` <br>
垂直对齐：vertical-align 取值：`top、middle、bottom、baseline	基线对齐` <br>
2、文字环绕 float <br>
文字环绕着图片进行布局，取值：`left、right`
### 九、背景样式
1、背景颜色 background-color <br>
2、背景图片地址 `background-image: url(图片路径);` <br>
3、背景图片重复 background-repeat <br>
取值：

    repeat	在水平方向和垂直方向上同时平铺（默认值）
    repeat-x	只在水平方向（x轴）上平铺
    repeat-y	只在垂直方向（y轴）上平铺
    no-repeat	不平铺
4、背景图片位置 `background-position: 水平距离 垂直距离;` <br>
水平距离和垂直距离取像素值或关键字（top left、center right、bottom center等） 
5、背景图片固定 background-attachment <br>
取值：`scroll 滚动（默认值）、fixed 固定不动` 
### 十、超链接样式
1、超链接伪类

    a:link{...}      定义a元素未访问时的样式
    a:visited{...}   定义a元素访问后的样式
    a:hover{...}     定义鼠标经过a元素时的样式
    a:active{...}    定义鼠标点击激活时的样式
定义4个伪类，必须按照“link、visited、hover、active”的顺序，不然浏览器可能无法正常显示这4种样式。 <br>
在实际开发中，通常只会用到两种状态：未访问时状态和鼠标经过状态 `a{...} 和 a:hover{...}` <br>
:hover伪类不只限用于a元素，它可定义鼠标经过任何元素时的样式 <br>
2、鼠标样式 cursor  <br>
取值：`default、pointer、text` <br>
自定义鼠标样式：`cursor: url(图片地址), 属性值;`  如：`cursor:url(img/cursor/default.cur),default;` <br>
属性值一般为3种：default、pointer和text
### 十一、盒子模型
* 所有的元素都可以看成一个盒子 <br>
盒子模型是由四个属性组成的：content（内容）、padding（内边距）、border（边框）、margin（外边距）<br>
#### 1、内容区 content：呈现了盒子的主要信息内容，这些内容可以是文本、图片等 
3个属性：width、height和overflow。width和height属性指定的是盒子内容区的高度和宽度（不包括内边距）；当内容过多超出width和height时，使用overflow属性来指定溢出处理方式。<br>
`只有块元素才可以设置width和height；行内元素设置的width和height无法生效，它的宽度和高度只能由内容区撑起来。`
#### 2、内边距 padding：指的是内容区和边框之间的空间，可以看成是内容区的背景区域
内边距的属性有5种：padding-top、padding-bottom、padding-left、padding-right以及综合了以上4个方向的简写内边距属性padding（顺时针，上右下左）。
#### 3、边框 border
#### 4、外边距 margin：两个盒子之间的距离，它可能是子元素与父元素之间的距离，也可能是兄弟元素之间的距离
外边距的属性有5种：margin-top、margin-bottom、margin-left、margin-right以及综合了以上4个方向的简写外边距属性margin（顺时针，上右下左）。<br>
* 当既有父元素，也有兄弟元素时，优先看四个方向有没有兄弟元素存在。如果该方向有兄弟元素，则这个方向的margin就是相对于兄弟元素而言。如果该方向没有兄弟元素，则这个方向的margin就是相对于父元素而言。

        脱离文档流的两种方法：浮动和定位
### 十一、浮动布局 float
清除浮动带来的影响：`clear: both;` （我们一般都是在浮动元素后面再增加一个空元素，然后为这个空元素定义clear:both来清除浮动。） <br>
此外还有overflow:hidden; 伪元素等方法
### 十二、定位布局 position
#### 1、固定定位：固定的元素不会随着滚动条的拖动而改变位置。
    position: fixed;
通过top、bottom、left和right这4个属性定义元素位置，这4个值的参考对象是浏览器的4条边，一般只会用到其中两个。<br>
固定定位最常用于实现“回顶部特效”
#### 2、相对定位：该元素的位置是相对于它的`原始位置`计算。
    position: relative;
通过top、bottom、left和right这4个属性来设置元素相对原始的位置，一般只会用到其中两个。   
#### 3、绝对定位
    position:absolute;
在几种定位方式中使用最为广泛，因为它能够很精确地把元素定位到任意你想要的位置。<br>    
一个元素变成了绝对定位元素，这个元素就完全脱离文档流了，绝对定位元素的前面或后面的元素会认为这个元素并不存在，此时这个元素浮于其他元素上面，已经完全独立出来了。<br>
* 默认情况下，固定定位和绝对定位的位置是相对于浏览器而言，而相对定位的位置是相对原始位置而言。
#### 4、静态定位 static
元素position属性的默认值是static。
