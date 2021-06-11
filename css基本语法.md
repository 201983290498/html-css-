# 标签

## 文本

### \<h1>

#### text-align 

文本的对齐方式

#### color

标题的颜色

### \<p>

段落

#### font

文字相关的设置

##### font-family

字体的设置, verdana

##### font-size

字体的大小





# 选择器

## 基本选择器

分为**id,class,标签**选择器

- id: #app
- class :  .class
- 元素:  el
- 通配符* 所有的意思

## 组合选择器

el.class 规定el下的class类

可以连在一起写

```css
h1, h2, p {
  text-align: center;
  color: red;
}
```

| 例子                                                         | 例子描述   |                                      |
| :----------------------------------------------------------- | :--------- | ------------------------------------ |
| [.*class*](https://www.w3school.com.cn/css/css_selectors.asp) | .intro     | 选取所有 class="intro" 的元素。      |
| [#*id*](https://www.w3school.com.cn/css/css_selectors.asp)   | #firstname | 选取 id="firstname" 的那个元素。     |
| [*](https://www.w3school.com.cn/css/css_selectors.asp)       | *          | 选取所有元素。                       |
| [*element*](https://www.w3school.com.cn/css/css_selectors.asp) | p          | 选取所有 <p> 元素。                  |
| [*element*,*element*,..](https://www.w3school.com.cn/css/css_selectors.asp) | div, p     | 选取所有 <div> 元素和所有 <p> 元素。 |

## 标签和class的关系

css层叠式样式

**一个标签里面可以匹配多个class,用空格分开**。

# css样式分类

## 外部样式

- 导入外部样式文件

- \<link rel="stylesheet" type="text/css" href="mystyle.css">

- 作用域:              整个网站的外观