# html

## 常用标签

### font字体

给段落中的字进行形式

属性 (键值对)：

- color 颜色

- size大小

### \<head>

不可见给浏览器解析用的

#### \<meta>

用来设置字符集的属性。避免乱码问题。

设置网页的元数据，就是最底层的数据。

Attributes:

```html
<meta name="keywords" content="htmls,css"><!--s-->
<meta http-equiv="refresh" content="300;url=https://www.baidu.com">
    <!--与http协议有关,refresh定义重定向,和指定的等待时间-->
```

### \<html>

#### 属性

lang : 显示页面的语言,其中zh为中文,en为英文

### \<h1>

​    一级标题-标签，网页搜索是最重要的东西。

#### \<hgroup>

​  给标签分组

### \<em>

​  语气的加重标签,是行内元素，不会独占一行

### \<strong>

​  表示我们强调重要的内容。

### \<blockquote>

​  表示常引用，块元素。

#### \<q>

​  引用元素,短引用。行内元素。

### \<p>

​  段落标签，不能嵌入块标签。

### 结构化元素

\<header>头部，可以有多个

\<main>主体,一个html只有一个

\<footer>底部,每个部分都可以有底部

\<nav>导航栏

\<article>表示文章

\<section>没有命名的区块

\<div> 区块

\<span>无语义，行内元素。

### 列表\<ul>\<ol>

​  \<ul>\<ol>无序列表，有序列表，\<li>列表项

​  \<ul>中有属性对type="none"可以去除前面的黑点。**他们都是块元素**

### 超链接\<a>

​  跳转到其他页面，或者跳转到该页面的其他位置。**是个行内元素，a标签中可以嵌套除了自身的任何元素**。

  常用属性:

​  target: \_self,\_blank **在原页面跳转还是打开新的窗口**

​   href: 超链接的地址，

​  业内跳转地址

​    ‘#’ 回到顶部：\<a href="#">回到顶部\</a>

​    '#id':跳到任意id处

​  可以使用**javascript:void(0);作为href的内容**，不会有任何作用

​    **text-decoration: none,** 将超链接的下划线去了

​  color: 设置字体

### \<img src=''>

​  **引入图片，属于替换元素，排版上像行内元素，基于块和行之间。**

#### 属性

- alt 图片的描述
- src图片的引用地址
- width指定宽度
- height指定高度，一般只会限定一个，然后等比例缩放

##### 图片格式

- jpeg:不支持动图，色彩丰富不支持透明效果，**透明效果就是指背景是否透明**,要来显示照片
- gif:颜色少，支持动图
- png:颜色丰富，支持复杂透明，不支持动图
- webp:专门用来表示网页中的图片的一种格式，具有所有优点，Google推出，**兼容性不好**

##### 超链接的本质

​  获取文本内容，并解析。

##### base64

将图片使用base64来编码，转换成字符，然后通过s**rc=文字**引入,一般只有网页需要一起加载的时候才这么用。

**通过网站将图片转成base64.**

### 内联框架\<iframe>

​  **在网页里面引入其他网页。**属于替代元素。

### \<audio>,\<vedio>音频视频

​  默认不允许用户操作的，代替元素。

#### 属性

- controls:允许控制。不需要值。
- autoplay:自动播放,不需要填值**,有的浏览器不支持**
- loop:不需要填值,循环播放

可以写成一下形式:

```html
<audio controls>
    <source src=''>
    <source src="">
    <embed src='' type='' width='' height=''> 适用于所有音视频的标签，不能停止或是其他缺陷，解决兼容性问题
    当有多个文件时，从上到下找可以使用的第一个文件
</audio>
```

### \<figure>

引入流对象,其中包含一个特殊子标签\<figcaption>代表标题

### \<details>

点击下拉显示细节,其中有个特殊子标签\<summary>显示为下拉前的字

![image-20210508221238718](C:\Users\coder\Desktop\数模学习\学习专用\image-20210508221238718.png)

### 常见属性

#### title

元素背后的文字，**当我们鼠标放到元素上去的时候显示的内容**。

## 基础知识

​    不同版本的html声明，我们用<!doctype html>说明是html5版本的语言，写在网页最开头。

​  字符的编码和解码需要字符集，我们用万国码utf-8

​  vscode自动生成基础文档`!+TAB`

​  html负责页面的结构，表现形式是css,我们更加关注的是**语义**

​  lorem自动生成一文本

### 块元素

页面中独占一行的元素（block element）;

**常见的块标签有,**

- \<h1> 标题标签
- \<p> 段落标签

  块元素主要用于布局，块元素能放任何元素。

**常见的行类元素(内联元素):**

- \<em>语气加强标签
- \<strong>强调标签

​  主要用来包裹文字

#### 属性

分为两种存型的，还有一种是需要键值对型的，例如，audio的controls

#### 转义字符

​  有时我们要用特殊字符，需要用到这些实体，可以利用实体的语法：`&+实体的名字;`例如`&nbsp(空格);`  `&gt;`  `&lt`大于号和小于号

#### 网页自动修正

​  浏览器会自动纠正代码，例如**标签写在了html的外部，p标签里面包含了块级元素。**

# css3

**html控制结构，css层叠样式控制，js控制行为。**

## 常用的使用方式style属性

1.所有标签中都可以用style样式

```htm;
   <p style="color: red;font-size: larger;">不同的属性间用封号隔开</p>

```

开发的时候不要使用**内联样式**，**内联样式值style写在标签里面。**

2.内部样式表

在head标签里面使用\<style>样式,**利用css选择器选中**.

**缺点**：只对一个页面起作用

3.外部样式表

​  把样式写成css文件，然后用**link**标签引入，**可以被多文件复用**。

```html
<link rel="stylesheet" href="./style.css">
stylesheet，表示样式表
```

## css选择器

1. 常用选择器

- 标签元素，直接写标签名，作用于所有的同类标签

  ```html
      <style>
          p{
              color: red;
              font-size: 20px;
          }
      </style>
  ```

- id选择器

  ```html
  #id{
  }
  用重复的id,都会变成红色，但是一般每个id都是不同的,js中选择id只会找一个元素，所以我们用class属性来应用于多个元素。
  ```

- class选择器

  ```html
  .class{
  
  }
  通过class使用多个样式格式如下
  <span class="blue red"></span>
  ```

- 通配选择器*

  ```html
  *{
  
  }
  作用于所有元素。
  ```

2. 复合选择器

   多个条件的选择器，例如既要是div标签，又要使用了classname类的样式。

- 交集选择器`标签.classname`

  ```css
  div.red{
      
  }
  //同时是div使用了redclass
  选择同时符合多个条件的元素。并列在一起代表同时满足
  .c.b.a{
      
  }
  只有同时用三个类的才可以选择：
  条件并列时的顺序为:标签名+id+class,
  ```

- 并集选择器，同时选中多个选择器，逗号隔开,然后赋值

  ```css
  h1,span,#id,.classname,..{
      color: green;
  }
  ```

3. 关系选择器

- 子代选择器

  ```html
  div > p > span{
    color: red;
  }
  有> 只能逐层搜索
  
  div span{
    color: red;
  }
  如果没有>,而是black，那么是指该标签下的所有子标签
  
  span{
    color: yellow;
  }
  当三种同时存在时:
  1.div span;div > span 同级，去最后一次的样式
  2.span,简单选择器的优先级低于关系选择器
  并列选择器和后代选择器并列锁定：
  div.box > span
  
  ```
  
- 2.后代选择器

  ```html
  div span{
  选择所有的span,范围广
  }
  ```

- 3.兄弟选择器

  ```html
  选择下一个兄弟;
  p + span{
    选择p下一个标签是span的span标签
  }
  
  p ~ span{
    选择与p同级的所有的span标签。只有p后面的span才会被选择。
  }
  ```

4. 属性选择器

- [属性名]指定还有指定属性的元素

  ```html
  (*)[attri]{
  
  }
  ```

- [属性名=属性值]xua'z

  ```html
  span[title=abc]{
      color: blue;
  }
  [title=abb]{
     color: red;
  }
  ```

- [属性名^=属性值]选择属性值以指定值**开头**的元素

- [属性名$=属性值]选择属性值以指定值**结尾**的元素

- [属性名*=属性值]选择属性值**含有**属性值的元素的元素

```css
        span[title=abc]{
            color: blue;
        }
        [title=abb]{
            color: red;
        }
        [title^=a]{
            font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
        }
        [title*=a]{
            font-size: 20px;
        }
```

5. **伪类选择器**和伪元素选择器

   前面都带‘:’,**一个**冒号伪类选择器，**两个**冒号伪元素选择器；伪类用来描述元素的一种特殊状态：**一般是第一个元素或者被点击的元素或者鼠标移入的元素。**

   常见的伪类:

   ​  :first-child 第一个元素

   ​  :last-child最后一个元素

     :nth-child(k) 选中第k个子元素，

   ​    如果选择n，则全部选中,

   ​    2n/even代表所有的偶数，

   ​    2n+1或者odd,所有的奇数.

    以上伪类主要**同一级别所有元素中进行排序**

   ​  :first-of-type 

   ​  :last-of-type

     :nth-of-type

   以上伪类元素与上面的类似，不同的是,**他们只对同一类的元素进行排序**

    :not()否定伪类，除了

   ```html
   li:not(:nth-child(3)){
       font-weight: 300;
   }
   ```

6. 超链接伪类

   ```html
   a:link{
    color: red;
   }没访问过的连接(所有的link)
   a:visited{
    color: blue;
   }访问过的连接
   :visited只能修改颜色，为了保护隐私,不让人很容易的知道。
   :hover 当鼠标移入的时候的式样，适用于多个标签
   :active 当鼠标点中时的样式，适用于所有元素
   ```

7. 伪元素选择器

   伪元素表示的是一些并不真实的元素（特殊的位置，例如每段的第一个字母）,相当于系统自己加了一个标签,然后选中样式

   ​  ::开头

   ​  ::first-letter 第一个字母

   ​  ::first-line 第一行

   ​  :: selection 被选中的元素

   ​  ::before 元素的开始,例如p中第一个字母前面的位置

   ​  ::after 元素的最后,最后一个字母之后的样式

   ​    before和after必须 和content结合使用，自己设定内容，且选不中

   ```css
           p::first-letter{
               font-size: 40px;
           }
           p::first-line{
               background-color: yellow;
           }
           p::selection{
               background-color: red;
           }
           p::after{
               content: 'huangjingwang';
               color: aqua;
           }通过css往元素中加元素,是个行内元素
   
   可以设置纵向长度，无法设置高度
   
   ```

## 选择器的权重

**样式冲突**：通过**不同的选择器**选择了**相同**的元素，设置了**不同的样式**。

优先级:
**内联选择器: 1000**
**id选择器: 100**
**类或者伪类选择器: 10**

**元素选择器: 1**
**统配选择器: 0**
**继承的样式没有优先级**

当出现**复合选择器**的时候:我们**优先级相加**得出优先级,例如div#id ,但是优先级不会**跨域**。

同级后出现的覆盖先出现的。

!important:在样式后面加上!important，优先级最高。

## css语法

\<style>标签中的区域要遵循css的规范。

**包含最基本的两大块，选择器和声明块，通过选择器，选中指定元素。**

声明块中，包含了对多`样式名: 样式值;`组成。

## 继承

**大标签的样式可以继承到子标签**里面里面。

并不是所有的样式都会被继承: **例如背景相关的，布局相关的。span背景是透明的。**

如何**样式是否**能被继承:

## 注释

/*xxxx*/

## 单位

### 大小单位

- 像素:具体大小

- 百分比：相对于父元素的百分比。会自动转换成像素溢出

- cm：厘米

- em: 一个字体的大小: 1em = 1 font-size，font-size可以自己定义

- rem:相对于根元素的的字体大小，就是html默认的

```css
        html{
            font-size: 20px;
        }
```



![image-20210509224031624](C:\Users\coder\Desktop\数模学习\image-20210509224031624.png)

### 颜色单位:

- 0~255,%

- rgb(red,green,blue,透明度)

  透明度：0全透明

- #xxxxxx十六进制表示法。

### HSL,HSLA

H 色相 0~360

S 饱和度 0%~100%

L 亮度，0%~100%

A:透明度

不同的颜色显示模型

```html
backgroup-color: hsl(0,100%,0%)
 hsla(0,100%,0%,透明度)
```


# 页面的布局

## 文档流

- 网页是个多层结构

- css可以分别给每层设置样式

- 用户看到的是顶层

- 最底层为文档流

  我们所创建的元素默认在文档流中进行排列。

- 元素有两种状态：在于不在文档流

元素在文档流中的特点：

- 块元素
  - 默认独占一行
  - 默认宽度父元素100%
  - 默认高度被内容(子元素)撑开

- 行内元素
  - 只占自身大小
  - 默认自左向右水平排列，容纳不下，自动换行

## div盒模型

​	    css把所有的元素都设置为一个**矩形**的盒子。

​	**对网页的布局就是将矩形摆放到不同的位置**

### 1.盒子的组成：

- 内容区（content），通过width和height控制大小
- 边框(border)
- 内边距(padding)'
- 外边距（盒子与盒子的距离，盒子的位置）

### 2.盒子的属性

```css
.box{
    width: 100px;//内容的大小
    height: 200px;
    backgroud-color: red;/*覆盖内容区和内边距*/
    /*border*/
    border-width: 10px;/*可以在中间加方位*/
    border-style: solid;
    border-color: red;
}

border简写属性
.box{
    border: 10px solid organe;
}
s
内边距padding:
padding-top:
padding-left:
padding-buttom:
padding-right:
padding内边距的简写属性，
盒子的大小为总大小


外边距:margin

百分比为父元素的总大小，
margin-xxx:
left和top移动自己
button和right:别人移动
margin-right:不会产生任何效果,因为是块级元素,同行没有其他元素
margin的简写:
影响盒子实际的大小。
负值反向移动，

background-color，覆盖边框，内边距和内容
backgroud-clip，限定background的范围。

```

- border-width :10px 20px 30px  40px: 可以省略不写，默认边框大小2~3px,顺序**上右下左**，**当缺省的时候（只有三个值或者2个值）缺省的上下相同，左右相同**

- border-top-width:上边的边框宽度（border-xxx-width），

- border-color**不写默认使用color属性的值**，color是浅景色,

- 以上三种都可以是四个值，且**都可以在中间加方位**

- border-style:

  - solid 实线
  - dotted 点状虚线
  - dashed 虚线
  - double双划线
  - 默认值none
  
- **color:前景色**

### 3.水平方向的位置布局:

由一下几个属性共同决定:

- margin-left
- border-left
- padding-left
- width
- padding-right
- border-right
- margin-right

一个元素在其父元素中，**必须要满足上面七者和为父元素内容宽**。如果不满足，则称为过度约束，等式会自动调整。**会自动调整margin-right使其满足换行**；

- 调整情况：

     **如果没有auto，调节margin-right**

     **这七个之里面有三个值可以设置成auto：width,margin-left,margin-right;有auto调整auto满足等式**

   ​  width:auto，除去已经定义的的宽度，全部是width,默认是auto:

   ![image-20210510170242264](C:\Users\coder\Desktop\数模学习\image-20210510170242264.png)

   ​  ![image-20210510170259390](C:\Users\coder\Desktop\数模学习\image-20210510170259390.png)

   **如果将一个宽度和外边距设置为auto,则宽度会最大，设置为auto的外边距自动为0.**

   **三个值为auto,外边距为0，宽度最大**

   **左右外间距为auto，居中**：margin: 0 auto,水平居中。

   **margin可以是赋值使得等式满足**

### 4.垂直方向上的布局

​  **父元素大小没定的请款下，由他的子元素大小决定，子元素超过父元素大小溢出会**，

​  **父元素有个属性overflow,解决溢出**

#### overflow

- visible: 可以看到溢出
- hidden:溢出的内容隐藏，不可见
- srcoll，生成滚动条，两个方向滚动条
- auto ： 根据需要生成滚动条。

##### overflow-x/overflow-y

​  单独处理两个方向

##### 外边距的重叠:（需要相邻,垂直方向）

- 兄弟元素

​  上一个元素margin-button和下一个元素的margin-top会发生重叠现象，**选择较大的外边距，有负值反向移动，一正一负取两者的和。同号取较大值**

- 父子元素

  子元素的margin-top会传递给父元素，

  导致整体向下,改用padding,父元素的padding或者自己的padding，

  **或者两个外边距不相邻，父元素加border**

解决方法：***02浮动-05***

### 5.行内元素的盒模型\<span>

- **行内元素不支持宽度和高度**
- 行内元素可以设置padding，**但是不影响总体布局，只是遮盖**。
- 可以设置border,不影响布局，
- 可以设置margin，**垂直方向不影响，水平方向相加求和，不重叠**

### 6.行内元素\<a>

​  行内元素不支持宽度和高度，如果一定要设置，转换成块属性。（display属性）

​  行内元素换行会自动在html中添加一个空格

​  **行内元素支持设置margin和padding,但content的大小不能由自己决定**

### display

- inline：显示设置成行内元素
- **block:  显示成块元素**，会独占一行
- inline-block:行内块元素，不独占一行又可以是个盒子
- table  将元素设置为表格
- none **元素不在页面中显示**
- (行内元素不需要满足宽度定理)margin的auto失效

**行内元素可能有空格，因为我们html页面的回车导致的。**

### visibility:

用来设置元素的显示状态:

- visible 默认，正常显示
- hidden，隐藏，但依旧占据页面的位置。

### 7.盒子的大小box-sizing

  box-sizing指定height和width代表谁的大小

- box-sizing: content-box，默认，宽高指内容区的大小
- box-sizing: border-bos , 宽高指定为边框的大小

### 8.轮廓，阴影和圆角outline,box-shadow(边框常用属性) 

​  两者只显示效果，**不影响盒子的大小和整体布局**

​  outline的用法和border相似

​  box-shadow: 10px 10px 50px rgba; 水平偏移量，垂直偏移量，模糊半径(越大越模糊)，颜色。

​  border-radius: 10px;圆角。

​    类似的:border-top-left-radius,border-top-right-radius,border-botton-left....

## 浏览器的默认样式

浏览器自己具备默认样式，我们在编写网页时要去除默认样式，主要是PC端。

我们可以通过浏览器进行修改。

### ul中的属性

**list-style:列表的样式，**![image-20210510193810309](C:\Users\coder\Desktop\数模学习\image-20210510193810309.png)none消除前面的点。

消除浏览器的格式

```css
*{
    margin: 0px;
    padding: 0px;
}
```

## 02.浮动float

特点：

- 设置浮动后从文档流脱离，不再占文档流中的位置。

- 同样浮动的元素可以横向排列。
- 浮动元素不会从**父元素中移出来**。
- 浮动元素无法占其他非浮动块元素的区域
- **浮动元素不会超过前面的兄弟浮动元素**,不能排布在前面元素的前面。

### 1. 浮动元素和文字

图片不会盖住文字，我们可以用**来让文字环绕图片**

### 2.元素脱离文档流后的特点

块元素：

- 不在独占一行
- **大小为内容撑开的大小，或者 自己设置的大小**
- 不在区**分块元素和行类元素，可以之际设置大小**

### 3.高度塌陷问题

**高度塌陷指:当父元素不设置高度，有内容撑开时，子元素设置了浮动，导致子元素脱离 了 文档流，父元素就会高度塌陷。**

解决方法：BFC，**开启块级格式化环境**

- BFC是css中的一个隐含属性，**开启BFC的元素会变成一个独立的 布局区域**

- 元素开启BFC的方式

  - float:大小随内容变，而且脱离文档流，导致下面的内容上移

  - overflow:依旧是块级元素，效果最好，不能设置为visible

    **设置overflow之后的属性不会被浮动元素覆盖。**避开浮动的位置，占据一行

  - 将元素设置成行内块元素display属性

开启BFC以后的效果:

- 不会出现上外边距重叠的现象
- 不会被浮动元素覆盖
- 可以包含浮动的子元素

**设置overflow以后排布在浮动元素之后，然后占满全行。**

### 4.clear

**清楚浮动元素对当前元素的影响。** **清楚浮动元素对下方兄弟元素的影响。**

- clear: left,消除左边浮动元素对当前元素的影响
- clear: right，消除右边浮动元素对当前元素的影响
- both 两侧

原理：当前元素自动添加上外边距。

### 5.利用伪元素(::after)解决高度塌陷	

​    我们在内容区的**最后加上空内容div,来撑开内容区**,但是伪元素::after默认增加的是块内元素,我们可以通过display来修改展示的形式,并用clear清楚浮动元素对下方元素的影响。

```html
    <style>
        .box1{
            border: solid red 1px;
            /* overflow: hidden; */
        }
        .box1::after{/*在文档的最后加内容,内容要消除浮动元素对它的影响,就能撑开内容区*//*利用伪元素实现*/
            content: '';
            clear:left;
            display: block;
        }
        .box2{
            width:100px;
            height: 100px;
            float: left;
            background-color: rebeccapurple;
        }
</style>
        
        <div class="box1">
        <div class="box2"></div>
        <div class="box2"></div>
        <div class="box2"></div>
        <div class="box2"></div>
        <div class="box2"></div>
        <!-- <div class="box2 box3"> 
        </div> -->
      </div>

​  **也可以解决外边距重叠的问题。**
<style>
        .box1{
            width: 200px;
            height: 200px;
            background-color: #bfa;
        }
        .box1::before{
            content: '';
            display: table;
        }
        .box2{
            width: 100px;
            height: 100px;
            background-color: red;
            margin-top: 100px;
        }
    </style>
```

```html
<div class="box1">
<div class="box2"></div>
</div>
```

综合可以用clearfix

```html
.clear::before,.clear::after{
  content:'';
  display: table;
  clear:both;
}
```

table:块级元素，空的时候不占内容

# 3.定位position

- 定位是一种更加高级的布局手段
- 通过定位可以将元素摆放到页面的任意位置
- 使用position属性来设置定位

可选值：

- static 默认是不开启定位
- relative 开启元素的相对定位
- absolute 开启元素的绝对定位
- fixed 开启元素的固定定位
- sticky 开启元素的粘滞定位

## 1.position的常用取值

### 1.相对定位relative

​   **定位位置为元素原本的位置**,进行相对移动。

   **相对定位会提升元素所在的层级(浮动在上层)，但不脱离文档流，且不改变元素的性质（块级元素依旧是块级元素）。**

​   元素设置相对定位以后，**不设置偏移量元素不会发生任何变化**。如何设置偏移量(offset)。

- 偏移量(offset)下面都是单独的属性，**需要提前开启定位**

  - top: **定位元素**和**定位位置**上边的距离
  - bottom ：**定位元素**和**定位位置**下边的距离
  - left
  - right

  ```css
          .box2{
              width: 200px;
              height: 200px;
              background-color: orange;
              /* margin-top: -200px;
              margin-left: 200px; */
              position: relative;/*开启定位*/
              top: 100px;
              left: 100px;
          }
  ```

### 2.绝对定位absolute

#### 特点

- **定位位置为本身的包含块**

- 通过position: absolute开启绝对定位。
- 开启决定定位以后，位置不变
- 从文档流中脱离，下面的元素上浮被遮住
- 会改变元素的性质（脱离文档流），变成行内块

#### 包含块（containing block）

- **正常为离当前元素最近的祖先块元素**。
- 在开启绝对定位时，包含块为**离他最近的**开启了**定位的祖先元素**。
- 如果所有祖先元素**都没**开启定位，则相对于**根元素**定位

#### 偏移量

- top
- botton
- left
- right

### 03固定定位fixed

​  是一种**特殊的绝对定位**，唯一不同的是：**永远参考于视口(可视窗口)进行定位。**

​  **当下拉滚动条时，元素跟着移动。**

### 04粘滞定位sticky

和相对定位的特点基本一致。****

**当上下滚动到特定的位置的时候不在变化。**

### 05_绝对定位

​  绝对定位在原本的宽度等式中添加了两个新的内容

```bash
left+margin-left+padding-left+content+padding-right-margin-right+right = 所包含块的内容宽度(一般和相对定位一起使用)
```

​  **在七个属性中能设置默认值的是left+right,margin,content。当left+right默认为auto，此时letf为0，right为最大值，当margin两个默认值时，居中，当left+right和margin都为auto时，前者的样式优先级大于后者。当三个一起的时候，width的auto有效。**

### 06_层级设置z-index

- z-index相同的时候，hmtl文件中后写的元素覆盖先写的元素
- z-index不同时，越大，优先显示
- 子元素z-index继承父元素的z-index且一定比父元素大一些

## 4.字体(font)与背景(backgroud)

### 1.常见属性

```html
<!-- 字体颜色-->
color

<!--字体大小 -->
font-size

<!--设置字体-->
font-family:(多值属性,从前往后挑选可用的)
可选值:
  - serif : 衬线字体 含有笔锋
  - sans-serif: 非衬线字体
  - monospace: 等宽字体 每个字母的宽度相同


<！--简写设置字体*/-->
font: [bold] [italic] (font-size)[/(line-height)] (font-family);
    省略会使用默认值，会覆盖之前的值

<!--字体加粗-->    
font-weight:  bold/normal;加粗/默认值，不加粗
    - 可以选100~900代表九个加粗的加别，100~500效果相同，没啥用，因为想要加粗，需要有两种加粗前后的两种字体。所以100~500效果相同用的是同一款字体。

    
font-style: normal/italic;正常(默认值)/斜体
    
```

- serif:![image-20210524133733908](C:\Users\coder\Desktop\数模学习\学习专用\image-20210524133733908.png)
- cursive :草书

上面的四个属性为大的字体分类，具体字体需要自己再写

### 2.引入自定义字体font-family&@font-face

@font-face

```css
@font-face{
  font-family: "(字体名字)myfont";
    <!--字体路径，格式包括了，ttf，woff,woff2,truetype等， -->
    src: url('./font/name.ttf') format("ttf")[,
        url() format()];
}
```

​  **src为多值属性，为的是让浏览器可以解析，从前往后选一个可行的。**

### 3.图标字体(iconfont)

​  最常用的网站为阿里的图标库，阿里巴巴矢量图标库，我们先介绍font awesome。

步骤：

- 下载
- 移除css和webfonts
- 用link引用css

使用图标字体的三种方式：

- \<i>标签+class引用

  class格式 ： `fas/fab 具体图标`

  ```html
  <i class="fas fa-bell"></i>
  ```
  
  可以设置font-size,color,向字体一样

- 通过伪元素实现

  ​  每个图标字体都有编码，可以通过转义图标字体的编码实现

  ```html
      <style>
          li{
              list-style: none;
          }
          li::before{
              content: '\f1b0'; /*图标字体的编码*/
              font-family: 'Font Awesome 5 Free'; /*说清楚是哪种字体*/
              font-weight: 900;  /*照抄，一定要*/
              color: blue;
              margin-right: 10px;
          }
      </style>
      <ul>
          <li>锄禾日当午</li>
          <li>汗滴禾下土</li>
          <li>谁知盘中餐</li>
          <li>粒粒皆辛苦</li>
      </ul>
  ```

  ![image-20210524141905931](C:\Users\coder\Desktop\数模学习\学习专用\image-20210524141905931.png)

- 第三种：在html页面中写

  ```html
  fab为font-family的css表示，是用来规定字体类的
  <span class="fas">&#xf0f3</span>
  通过实体来使用 &#x图标编码
  
  ```

### 4.[阿里字体库](https://www.iconfont.cn/)

下载出来

```css

<link rel="stylesheet" href="../static/ali/font_2567255_uylicf0z4j/iconfont.css">
设置字体大小
然后可以通过三种方式引用
```

### 5.行高line-height

  通过line-height来设置行高，如果是个不带单位的数，将是字体的倍数。默认值为normal

​  所有的字体都有**一个字体框**，行高会在字体框上下平均分布。

### 6.文本的样式

**对齐样式**：**text-align**，水平对齐

```html
left/right/center
jusity 两端对齐，通过扩大字体之间的空格做到

```

**行内元素垂直对齐**：verticle-align

```hmtl
baseline: 基线对齐,基线为字体框的线（默认）
middle：子元素的中线和X字母的中线对齐
top/bottom： 顶部/底部对齐，对齐每一行的顶部和底部
100px
```

​    **图片也是默认是沿着基线对齐，我们可以用verticle-align解决**

**文本修饰：** text-decoration

- none 无，默认
- underline 下划线
- line-through,删除线
- overline 上划线
- 格式还可以加颜色 overline red;

**处理空白：**white-space

- normal  正常, 不够最后的自动换行
- nowrap 不换行，
- pre： **保留html中所有空格**，默认的html中多个空格自动合并成一个空格

**文本超出div处理**: text-overflow:

​      overflow: *hidden*;

​      text-overflow: *ellipsis*;同时设置

## 5.背景

### 5.1常见属性

- background-imgae:背景图片,
  - 背景 图片小于元素，会自动铺满
  - 背景图片大于元素，将有一部无法完全显示

- backgroud-color: 背景颜色
- backgroud-repeat: 设置背景的重复方式
  - repeat :默认值，双向展开重复
  - repeat-x
  - repeat-y
  - no-repeat:不重复
- background-position: 设置背景图片的位置，一般用于不重复的背景
  - top,left,center,bottom,right(需要两个值定位，不写第二个默认第二个为center)
  - 偏移量：水平方向偏移量，垂直方向偏移量
- background-clip: 背景范围
  - border-box
  - padding-box
  - content-box
- background-origin:背景图片开始铺设的原点
  - padding-box
  - content-box
  - border-box

- backgroud-size:背景图片的大小,当图片的大小超过背景框本身的时候。

```css
background-image:url("");
background-color:
background-repeat:
background-position: top center;
background-position: 10px 10px;
```

​  对于backgroud-size如果我们设置一个值，另一个值为auto，那么auto的值会自动适应。，可能导致的结果就是适应的维度超出背景框的范围。所以还有一个属性contain 图片的比例不变，完整的显示在背景框中。

- backgroud-attachment: 背景是否与文字的吸附方式，可选值如下:
  - fixed:  固定以后可以通过xxx- position调整位置
  - scroll: 随着文字滚动。
  - 当content-box的内容超过内容盒子本身的大小的时候，overflow属性可以设置滚动条。
- 统一简写属性background：可以填上面的所有属性的值，为了加以区分，我们规定背景的位置和大小要写成如下的样式 center center/contain， 背景的源点和背景的显示范围先写原点的范围,再写一个背景的范围。

样例：

```html
背景图片自适应大小，且全局居中：
- 需要先设置不重复，单个图片的位置
- 在设置背景图片的大小为contain(包含)
```

## 6.背景颜色渐变

### 6.1 线性渐变

  使用的属性background-image: linear-gradient(dir,color1,color2,color3....)

- dir 可以是to right
- dir 默认是从上向下
- dir 可以设置成度数： 20deg deg表示度数
- 渐变可以指定多个元素，每个元素默认平均分布

  同时我们也可以设置渐变的宽度。例如：

```css
  background-image: linear-gradient(dir,color1 width,color2 width2)
  /*width1代表渐变的起始位置，前面的是纯色,color2从width2开始是纯color2,上面是渐变色。只有第一个颜色前面是纯色，因为上面没有颜色。*/
```

  下面我们介绍重复的线性渐变。值为repeating-linear-gradient(red 50px,yellow 100px),说明50是纯红，100是纯黄，渐变色的宽度为50，其他地方会自动平铺，因此，它的效果其实和background-image: repeating-linear-gradient(red,yellow,50)效果相同。

### 6.2径向渐变

  径向渐变也是background-image的一个属性值，radial-gradient(red,yellow),颜色从中心向外变化。
  径向渐变的长短轴为默认为背景图的长短轴，，超出半径的是纯色，我们也可以自己调节半径。
  background-image: radial-gradient(100px 200px,red,yellow)先设置宽，再设置高。
  还有些关键字，例如我们渐变的中心不在中心点，有所偏移，这时候我们可以限定渐变的范围，就是大小既可以是一个元组，或者是一个英文关键字，可选值:

- closest-side,渐变到最近的边
- closeet-corner,渐变到最近的交
- farthest-side,远边
- farthest-corner,远角

  位置的关键字:top,button,left,right

  