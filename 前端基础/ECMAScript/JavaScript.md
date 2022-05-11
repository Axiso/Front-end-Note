

# 简介

**JavaScript 最初是作为 HTML 的脚本扩展而开发的，而现在已经成为浏览器中运行的唯一通用语言。如今它也被用到了很多非浏览器环境中，例如 Node.js、 Apache CouchDB 和 Adobe Acrobat。**

维基百科：[JavaScript](https://zh.wikipedia.org/wiki/JavaScript)  
JavaScript ( JS ) 是一种具有函数优先的轻量级，解释型或即时编译型的编程语言。JavaScript 是一种基于原型编程、多范式的动态脚本语言，并且支持面向对象、命令式和声明式（如函数式编程）风格。JavaScript 可以用来操控文本、数组、日期以及正则表达式等。不支持I/O，比如网络、存储和图形等，但这些都可以由它的宿主环境提供支持。


一般来说，完整的JavaScript包括以下几个部分：
1. ECMAScript，描述了该语言的语法和基本对象
2. 文档对象模型（DOM），描述处理网页内容的方法和接口
3. 浏览器对象模型（BOM），描述与浏览器进行交互的方法和接口

---

文档对象模型（英语：Document Object Model，缩写DOM），是W3C组织推荐的处理可扩展置标语言的标准编程接口。

浏览器对象模型(BOM)指的是由Web浏览器暴露的所有对象组成的表示模型。BOM与DOM不同，其既没有标准的实现，也没有严格的定义, 所以浏览器厂商可以自由地实现BOM。

链接：  
[DOM](DOM.md)  
[BOM](BOM.md)  


参考链接：  
[JavaScript 参考](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference)  
[什么是 JavaScript？](https://developer.mozilla.org/zh-CN/docs/Learn/JavaScript/First_steps/What_is_JavaScript)  
[DOM概述](https://developer.mozilla.org/zh-CN/docs/Web/API/Document_Object_Model/Introduction)

# JavaScript 与 ECMAScript
ECMAScript 是一种脚本语言规范（标准），其形成主要来自于 JavaScript 的实际应用。（实践先于理论，类似于OSI七层模型和TCP/IP五层模型的关系）

而 JavaScript 可以看作是一种 ECMAScript 方言（类似于SQL规范与MySQL方言），是 ECMAScript 的其中一种实现。但是其实JavaScript是先于ECMAScript出现的。

完整的JavaScript实现包含以下几个部分:
* 核心（ECMAScript）
* 文档对象模型（DOM）
* 浏览器对象模型（BOM）

ECMAScript 标准中不包含 DOM 和 BOM的定义，只涵盖基本数据类型、关键字、语句、运算符、内建对象、内建函数等通用语法。


## script标签
js要使用`<script>`标签来插入HTML中。  

script标签可以放在head标签、body标签、body标签

事件  
脚本  

不同的标签都有对应的事件属性

alert  弹框  
console.log  控制台打印    
document.write  在网页打印  

## js的数据类型

参考链接：[JavaScript 变量类型](https://developer.mozilla.org/zh-CN/docs/Learn/JavaScript/First_steps/Variables#%E5%8F%98%E9%87%8F%E7%B1%BB%E5%9E%8B)


最新的 ECMAScript 标准定义了 8 种数据类型，分为基本类型和引用类型。

基本类型：  
* string  
* number  
* boolean  
* BigInt  
* null  
* undefine  
* symbol

引用类型：  
引用类型统称为 Object 类型。包括：  
* Array  
* Date  
* Math
* RegExp  
* function  
* ...



# var、let、const
全局变量，局部变量？？？有作用域，没有作用域？？？
> var 声明的变量没有作用域，let 声明的变量有作用域。  
> 在同一个作用域内，var 可以多次声明同一个变量名，let 只能声明一次。  
> const 声明的变量为常量，而且是局部常量，初始化之后不能再次改变。且定义时就要进行初始化。  


---
变量定义：  
```js
<script type = "text/javascript">
   var name = "毛小帅";
   var age = 10;
   var height = 183.5;
   var isMarred = false;
   var girlFriend = {
       name : "lxs",
       age : 19
   }
   var print = function(){
       console.log("哈哈哈");    
   }
</script>
```


## 运算符
---
赋值运算符: =  

---
算数运算符: + - * / % ++ -- 

---
逻辑运算符:  
&&	逻辑与  and  
||	逻辑或  or  
!	逻辑非  not  

---
比较运算符:    
==  等于 只要值相等就相等  
===  全等 不仅要值相等，类型也要相等  

---
三元运算符：

---
类型运算符:  
typeof	返回变量的类型。  
instanceof	返回 true，如果对象是对象类型的实例。

## 程序结构

循环结构：while循环；for循环；forin循环  
分支结构:switch语句；  

```js
<script type="text/javascript">  
    var arr = [1,2,3,4,5];
    for(var i in arr){
        console.log(i);
    }
</script>
```

## 函数定义

js中定义函数时不需要指定返回值类型，参数列表也不用指定类型，因为js所有的类型都是var。

function 方法名(参数列表){
    方法体;
}

```js
// 参数列表不需要声明类型

function func(parameter1，parameter2){
    函数体;
}


function(parameter1，parameter2){
    函数体;
}

```

## 事件绑定
js中事件的分类：鼠标事件、键盘事件、表单事件

常用事件：
| 事件     |             |
| -------- | ----------- |
| 表单事件 | onblur()    |
|          | onfocus ()  |
|          | onchange () |
| 鼠标事件 | onclick()   |
| 键盘事件 | onkeyup     |
|          | onkeydown   |


js对象.事件名称(function(){
    方法体;
})
```js
//获取到用户名的输入框
var userNameInput = document.getElementsByTagName("input")[0];
//输入框的失焦事件
userNameInput.onblur = function() {
//获取到输入框中输入的内容
var username = this.value;
if (username == null || username == "") {
	mistake(userInfo, "用户名不能为空");
} else {
	if (username.length < 6 || username.length > 15) {
		mistake(userInfo, "用户名的长度为6~15，不满足！");
	} else {
		correct(userInfo, "用户名ok!");
	}
}
}
```

```js
setInterval(function () {
   $("#d1").text(num);
   num++;
}, 1000);
```

# this

this 在nodejs环境下默认为空对象，在浏览器环境下默认为Windows对象。  

<img src="../pic/JavaScript/this2.png" width="80%" >  
<img src="../pic/JavaScript/this1.png" width="80%" >  

---

对于在HTML文件中new出来的 Vue 对象，Vue的 data、method 中的内容全部直接属于Vue对象，可以直接调用，不需要再经过data、method。

html 源代码：[Vue 中的 this](../Source%20Code/前端/HTML/vue_this.html)
<img src="../pic/JavaScript/vue_this.png" width="80%" >  
分别输出两个 this，一个是Window对象，一个是Vue对象  
<img src="../pic/JavaScript/vue_this2.png" width="80%" >  
从下面两个图可以看出，Window对象中包含 Vue 对象， 而 Vue 对象中的属性 (`name`、`gender`) 
以及方法 (`print_this`) 直接属于 Vue 对象 ，而不是 data和method。
<img src="../pic/JavaScript/vue_this3.png" width="80%" >
<img src="../pic/JavaScript/vue_this4.png" width="80%" >


# 

随机整数：
parseInt(Math.random()*(b - a + 1)) + a



