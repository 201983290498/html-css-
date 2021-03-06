# HTML

<a>代表超链接

<a href="">指定链接的地址

标签，属性，属性值的大小写不敏感。

属性值应该用引号引起来

## 1.常用标签

### 1.1<h>标题标签h

#### 属性

- **align="center"**对齐方式
- **bgcolor="yellow"**



**注释**：浏览器会自动地在标题的前后添加空行。

**注释：**默认情况下，HTML 会自动地在块级元素前后添加一个额外的空行，比如段落、标题元素前后。



-----------

### 1.2 <body>标签body

#### 属性

- **bgcolor="yellow"**背景颜色



-----------

### 1.3<table>表格table

#### 属性

- **border="1"**边框的附加信息





----

### 1.4 <hr />标签水平线

创建水平线，用于分割内容



### 1.5 注释内容

行如<!-- 表示注释内容 -->；



-----

### 1.6文档头部head

<head>
<title>头部的标题</title> 窗口的名字
</head>





---------

### 1.7段落p

<br />  可以插入一个空行

p是块级属性，自动在前面加换行







-------



## 2.属性

全局属性，任何标签都能有的属性

![image-20210226164745814](C:\Users\coder\Desktop\数模学习\图片\image-20210226164745814.png)

**style属性可以改变元素的样式**

样式里面有很多的属性，

字体大小：font-size

字体font-family，字体样式

color颜色，不同属性用封号隔开

## 注意事项

浏览器会自动过滤多余的空格和换行





## 3.常用格式标签

```html
<blockquote>
长引用
 
</blockquote>
<q>
短引用
</q>
<cite>
定义引证论证
</cite>
<dfn title="">
定义一个概念
</dfn>
我们对缩写，定义，首字母缩写通过title属性输入原字符窜



计算机代码
<samp>元素定义计算机输出字符</samp>
<kbd>定义从键盘中获得的字符</kbd>
<code>不保留多余的空格和折行</code>
<var>定义数学变量</var>


注释：条件注释
<!--[if IE 8]>
...Some HTML heree...
<![endif]-->
条件注释定义只有 Internet Explorer 执行的 HTML 标签。

```


HTML 计算机代码格式

通常，HTML 使用*可变*的字母尺寸，以及可变的字母间距。

在显示*计算机代码*示例时，并不需要如此。

*<kbd>*, *<samp>*, 以及 *<code>* 元素全都支持固定的字母尺寸和间距。



### 3.1CSS

**通过使用 HTML4.0，所有的格式化代码均可移出 HTML 文档，然后移入一个独立的样式表。**



[HTML中的样式](https://www.w3school.com.cn/tiy/t.asp?f=html_style)

本例演示如何使用添加到 <head> 部分的样式信息对 HTML 进行格式化。