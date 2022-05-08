$
:
[]

任何需要使用脚本的地方都需要绑定事件

脚本需要有触发条件  事件



jQuery的核心对象： $ 或 jQuery  

jQuery中获取input输入框中的内容的方法 value() ,获取下拉选择框中的内容的方法 val()

## jQuery选择器

美元符号、括号、双引号

基本选择器:  
标签选择器 `标签名`  
id选择器 `#`  
类选择器 `.`  
> 类似于CSS的选择器

```javascript
<body>	
    <div id="d1" class="c1"></div>
    <div id="d2" class="c2"></div>
    <script type="text/javascript" src="/js/jquery-3.5.1.min.js"></script>
    <script type="text/javascript">
        // id选择器
        $("#d1").text("我是使用$的选择器");
        jQuery("#d2").text("我是使用jQuery的选择器");
        // 类选择器
        $(".c1").css("font-size","40px");
        jQuery(".c2").css("font-size","30px");
        // 标签选择器
        $("div").css("text-align","center");
    </script>
</body>
```
```javascript
$("#uname").blur(function () {
    var name = $(this).val();
    // this指代某个已经被选中的对象,比如这里表示id为uname的标签
    console.log(name);
    if(name=="" || name == null){
        $("#uname_msg").text("用户名不能为空").css("color","red");
    }else {
        $("#uname_msg").text("ok").css("color","green");
    }
})
```

> `.text()`是将文本内容显示在标签的一对尖括号中间

---
层级选择器：  
后代选择器 `空格`  
子代选择器 `>`  
相邻兄弟选择器 `+`  同级以下紧挨着的  
一般兄弟选择器 `~`  同级以下  

---
过滤选择器：使用冒号分隔，后面写过滤条件。  

表单过滤选择器

| 过滤条件  | 含义                            |
| --------- | ------------------------------- |
| :first    | 获取第一个                      |
| :last     | 获取最后一个                    |
| :eq(3)    | 选择指定索引的标签，索引从0开始 |
| :gt(3)    | 选择大于指定索引的标签          |
| :lt(3)    | 选择小于指定索引的标签          |
| :odd      | 奇数                            |
| :even     | 偶数                            |
| :enabled  | 没有被禁用的标签页              |
| :disabled | 被禁用的标签页                  |
| :checked  | 复选框中被选定的内容            |
| :selected | select标签中选择的内容          |
| :radio    |                                 |
|           |                                 |
|           |                                 |



---

## 事件绑定

常用事件：

| jQuery效果方法 | 效果                     |
| -------------- | ------------------------ |
| show()         | 显示                     |
| hide()         | 隐藏                     |
| toggle()       | 具有切换功能的显示和隐藏 |
| fadeIn()       | 淡入                     |
| fadeOut()      | 淡出                     |
| fadeToggle()   | 具有切换功能的淡入和淡出 |
| slideDown()    | 下拉显示                 |
| slideUp()      | 上拉隐藏                 |
| slideToggle()  | 具有切换功能的上下拉     |

| jQuery事件方法 |                             |
| -------------- | --------------------------- |
| bind()         | 向元素添加事件处理程序      |
| blur()         | 添加/触发失去焦点事件       |
| change()       | 添加/触发 change 事件       |
| click()        | 添加/触发 click 事件        |
| dblclick()     | 添加/触发 double click 事件 |
| submit()       | 添加/触发 submit 事件       |

显示与隐藏效果是通过改变宽高和不透明度来
淡入和淡出是通过改变css的hide和不透明度来实现的
上下拉只改变高度来实现，类似于投影仪的幕布。

## 操作css样式

通过修改
css({
    "样式名":"值"；
    "样式名":"值"；
    "样式名":"值"；
})

通过增加类来操作，
addClass() removeClass() toggleClass()

## jQuery的dom操作


# jQuery的Ajax操作
# jQuery使用Ajax

参考链接：  
[jQuery发送Ajax请求](https://blog.csdn.net/jinixin/article/details/80042763)

$.ajax  
$.ajax({name:value, name:value, ... })
```jsp

```

---
$.get  

语法
```
$.get(URL,data,success,dataType);
```

---
$.post  
语法
```jsp
$.post(URL,data,success,dataType);
```