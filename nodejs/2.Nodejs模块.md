

# 模块

引入模块
在 Node.js 中，引入一个模块非常简单，如下我们创建一个 main.js 文件并引入 hello 模块，代码如下:

```
var hello = require('./hello');
hello.world();
```

node中模块分类:
1. 核心模块
   由 node 本身提供，不需要单独安装（npm），可直接引入使用。

2. 第三方模块
   由社区或个人提供，需要通过npm安装后使用。

3. 自定义模块
   由我们自己创建，比如：tool.js 、 user.js

> 一个js文件就是一个模块。每个模块都是一个独立的作用域，在这个而文件中定义的变量、函数、对象都是私有的，对其他文件不可见。

核心模块
fs：文件操作模块
http：网络操作模块
path：路径操作模块
url: 解析地址的模块
querystring: 解析参数字符串的模块

<img src="../pic/nodejs/npm%20global.png" alt="image-20220507102430172" style="zoom:80%;" />

# import、export

模块化思想是从java上衍生过来的，他将所需要的功能封装成一个类，哪里需要就在哪里调用，JS中没有类的说法，但它引入了这种思想，在js中用对象或构造函数来模拟类的封装实现模块化，而在html上，则使用import和require


## require和import的区别
$ 调用时间
require 是运行时调用，所以理论上可以运作在代码的任何地方
import 是编译时调用，所以必须放在文件的开头
 

$ 本质
require 是赋值过程，其实require的结果就是对象、数字、字符串、函数等，再把结果赋值给某个变量。它是普通的值拷贝传递。
import 是解构过程。使用import导入模块的属性或者方法是引用传递。且import是read-only的，值是单向传递的。default是ES6 模块化所独有的关键字，export default {} 输出默认的接口对象，如果没有命名，则在import时可以自定义一个名称用来关联这个对象



