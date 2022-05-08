


$scope  
$event  
$http  


当在控制器中添加 $scope 对象时，视图 (HTML) 可以获取了这些属性。

视图中，你不需要添加 $scope 前缀, 只需要添加属性名即可，如： {{carname}}。






# 

html  jsp

html anglarjs js css


# AngularJS 官方文档


# 
[AngularJS](https://zh.wikipedia.org/wiki/AngularJS)


# AngualrJS 代码组成

[AngularJS的基本用法](https://objcoding.com/2017/06/03/AngularJS(1)/)

表达式  
指令  
服务  
controller  
service  
过滤器  



Angular本身也提供了很多非常优秀的服务，如＄Http，＄scope，＄routeParams，＄q等等，他们有个共同的特征，即前缀都是美元符号＄。


---
AngualrJS应用的组成：

veiw：视图，即html页面；
model：模型，即页面所需要的数据；
Controller：控制器，可以对模型的数据进行修改或添加或删除。

作用域：
前面我们有提到过作用域这东西，指的就是model，它是AngualrJS在HTML域JS之间传值的一个非常重要的东西，通常我们从后台请求回来的数据都会放在作用域中，然后HTML通过作用域拿到数据，展示给用户。
$scope只作用于其所在的控制器ng-controller包含的html。
$rootScope是根作用域，它作用于ng-app包含的html。

---
AngularJS 应用组成如下：

View(视图), 即 HTML。
Model(模型), 当前视图中可用的数据。
Controller(控制器), 即 JavaScript 函数，可以添加或修改属性。



scope 是一个 JavaScript 对象，带有属性和方法，这些属性和方法可以在视图和控制器中使用。


模型和视图




# 
AngularJS 代码由以下几种组成：  

使用angularjs需要引入js脚本，然后在HTML的body标签中声明 ng-app ，ng-app 指令 作用是告诉子元素一下的指令是归angularJs的,angularJs会识别的，ng-app 指令在网页加载完毕时会自动引导（自动初始化）应用程序。

## 表达式

## Angular指令（Directive） 

AngularJS 指令是扩展的 HTML 属性，带有前缀 ng-。

* ng-app 指令，用来初始化一个 AngularJS 应用程序。
* ng-controller 指令，给HTML页面指定一个应用程序控制器。
* ng-init 指令，用来初始化应用程序数据。
* ng-model 指令，把HTML页面中的元素值（比如输入域的值）绑定到model。
* ng-click 指令，
* ng-select 指令，
* ng-option 指令，
* ng-repeat 指令，

> AngularJS extends HTML attributes with Directives, and binds data to HTML with Expressions.  

AngularJS 使用Angular 指令来扩展 html 属性，使用 Angular 表达式来绑定数据到htl。

> **AngularJS Extends HTML**  
> AngularJS extends HTML with ng-directives.  
> 
> The ng-app directive defines an AngularJS application.  
> The ng-model directive binds the value of HTML controls (input, select, textarea) to application data.  
> The ng-bind directive binds application data to the HTML view.

AngularJS **扩展了** HTML  
AngularJS 使用angular指令 **扩展了** HTML  

AngularJS 指令是指由 `ng-` 开头的指令，被添加到 html 标签中作为属性。  
即，AngularJS 通过在 html 中添加 `ng-` 开头的 angular 指令来扩展 html。  

> The data model is a collection of data available for the application.

> The HTML container where the AngularJS application is displayed, is called the view.  
> The view has access to the model, and there are several ways of displaying model data in the view.  
> You can use the ng-bind directive, which will bind the innerHTML of the element to the specified model property.  
> You can also use double braces {{ }} to display content from the model.
> Or you can use the ng-model directive on HTML controls to bind the model to the view.

> Data binding in AngularJS is the synchronization between the model and the view.  
> When data in the model changes, the view reflects the change, and when data in the view changes, the model is updated as well.


## 服务

$scope
$rootscope
$http
$event
$watch

## 控制器

```js
app.controller('',function(){

})
```

控制器部分的代码就是js文件中，
语法是js语法和angular语法的混合

angular应用必须包含控制器，至于service、filter可根据需求

先声明模块，使用模块声明控制器，控制器使用方法和属性

可以将function括号内的看作变量，每次添加的服务




# 
模块、控制器




# 作用域

Angular数据绑定主要内容在于方括号[ ]，和圆括号（）还有花括号｛｝



```
$scope.mxs={};
$scope.mxs=[];
$scope.mxs='';
```

在js中绑定来自后端的数据
在html中绑定前端的数据

---

Angular 具有不同的表达式语法，主要是用 "[ ]" 来表示属性绑定，以及用 "( )" 来表示事件绑定[7]




























# 内部类

静态内部类
![](../pic/java/internalclass.png)



# 

