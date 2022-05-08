HTML (HyperText Markup Language) 不是一门编程语言，而是一种用来告知浏览器如何组织页面的标记语言。

以下内容全部基于 HTML5

---

从代码的格式上看，可以认为所有的 HTML 都是由以下几种组成的：  
* 标签  <>  
* 属性/事件  name、value  

HTML的所有特性都是基于这两点的，可能随着版本的更新，会在原版本的基础上增加新的标签，或者在原版本已有的标签上增加一些新的属性。

从属性的适用范围看，所有标签都可以使用的属性叫全局属性，每个标签独有的属性叫局部属性。  
还有一些属性是可以触发浏览器执行相应动作的，这种属性被叫做 事件属性。  


标签和属性的默认值；

> 对于初学者比较迷惑的点在于，虽然标签名和属性名都是经过严格定义的，但是每种标签有哪些属性却往往很难记忆。  
> 可以将标签名和属性名理解为两个集合，相互映射。  

# 参考文档

[HTML（超文本标记语言）](https://developer.mozilla.org/zh-CN/docs/Web/HTML)

# 

div显示出来的大小和设置的不一致的原因是系统默认缩放的问题。

浏览网页时，打开开发人员窗口，可以看到加载了很多文件，涉及的就是css和js外部文件的引入。

# 全局属性

比较常用的有：  
id、class、

# 单标签和闭合标签

## 单标签
`<link>`  

有些浏览器不支持单标签

## 双标签

除单标签以外的都是闭合标签

# 行级元素块级元素
行级元素：input
块级元素：

# 特殊字符
在HTML中，字符 <, >,",' 和 & 是特殊字符. 它们是HTML语法自身的一部分, 如果想要将这些字符包含进文本中，就必须使用字符引用 —— 表示字符的特殊编码。
每个字符引用以符号&开始, 以分号(;)结束.

| 原义字符 | 等价字符引用        |
| -------- | ------------------- |
| <        | `&lt;` less than    |
| >        | `&gt;` greater than |
| "        | `&quot;`            |
| '        | `&apos;`            |
| &        | `&amp;`             |


```html
&reg;	®	已注册
&copy;	©	版权
&trade;	™	商标
&gt;  
&lt;  
&nbsp;  
&copy;  
```

## 行内元素与块级元素


# 表单form
action 属性定义在提交表单时执行的动作。如果省略 action 属性，则 action 会被设置为当前页面。  
method 属性规定在提交表单时所用的 HTTP 方法(默认是get)  

```html
<input type="button">
<input type="checkbox">
<input type="color">
<input type="date">
<input type="file">
<input type="datetime">
<input type="datetime-local">
<input type="email">
<input type="hidden">
<input type="image">
<input type="month">
<input type="number">
<input type="password">
<!-- 指定了密码类型，在输入框内输入时就会在地址栏显示一个🔑图标 -->
<input type="radio">
<input type="reset">
<input type="search">
<input type="submit">
<input type="tel">
<input type="text">
<input type="time">
<input type="url">
<input type="week">
```

![](../pic/html/input.png)


enctype（encoding type）属性用来指定表单的编码类型；

## 表格table
[HTML_table](HTML_table.md)

| Tag | Description                                        |
| --- | -------------------------------------------------- |
| tr  | table row,Defines a row in a table                 |
| th  | table header cell,Defines a header cell in a table |
| td  | table data cell,Defines a cell in a table          |

```html
属性的设置作用范围，属性有默认值，属性的取值类型（数字，百分比）
align

<table cellspacing="0" cellpadding="10" border="" width="900" height="450" align="center">
    <tr>
        <th>姓名</th>
        <th>性别</th>
        <th>年龄</th>
        <th>生日</th>
    </tr>
    <tr>
        <td>姓名</td>
        <td>性别</td>
        <td>年龄</td>
        <td>生日</td>
    </tr>
    <tr>
        <td>石叡</td>
        <td>女</td>
        <td>21</td>
        <td>92381989</td>
    </tr>
    <tr>
        <td>PGone</td>
        <td>男</td>
        <td>32</td>
        <td>难上加难</td>
    </tr>
</table>
```

# 列表
## 有序列表ol

[docs/Web/HTML/Element/ol](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/ol)

```
<ol>
    <li>姓名</li>
    <li>年龄</li>
    <li>性别</li>
</ol>
```
---
ol有关属性：  

start  
一个整数值属性，指定了列表编号的起始值。此属性的值应为阿拉伯数字，尽管列表条目的编号类型 type 属性可能指定为了罗马数字编号等其他类型的编号。比如说，想要让元素的编号从英文字母 "d" 或者罗马数字 "iv" 开始，都应当使用 start="4"。

type 
设置编号的类型：  
a 表示小写英文字母编号  
A 表示大写英文字母编号  
i 表示小写罗马数字编号  
I 表示大写罗马数字编号  
1 表示数字编号（默认）  
编号类型适用于整个列表，除非在 `<ol>` 元素的 `<li>` 元素中使用不同的 type 属性。


## 无序列表ul

```html
<ol type="a" start="4">
    <li>姓名</li>
    <li>年龄</li>
    <li>性别</li>
</ol>
```

# 引入外部文件

```
<script src="../plugins/angularjs/pagination.js"></script>
<link rel="stylesheet" href="../plugins/angularjs/pagination.css">
```

script 用来引入 js 类库。  
link 用来引入 css 样式。  

还可以引入模板引擎
```
<!DOCTYPE html>
<html lang="en" xmlns:th="http://www.thymeleaf.org">
```



类比jsp:  
```
<%@ taglib prefix="c" uri="http://java.sun.com/jsp/jstl/core" %>
<%@ page contentType="text/html;charset=UTF-8" language="java" %>
```

# button、input、a 三者的区别

这三个标签都可以用来点击跳转，但是在使用上有差别：
* button 可以通过onclick或ng-click属性绑定javascript事件。  
  效果：<button onclick="location.href='add.jsp'" type="button" id="btn">点击跳转</button>
* input 可以通过 type="submit" 来将表单内用户设置或选择的所有数据一并提交到后台。  
  效果：<input id="login" type="submit" name="login" value="注册" style="width: 100px;"/>  
  是不是必须在form中用
* a 可以通过 href="#" 添加链接访问到页面中的某一个位置或另一个页面，不向后台提交数据。  
  效果：<a href="${path}/doctor/index.jsp">点击跳转</a>







