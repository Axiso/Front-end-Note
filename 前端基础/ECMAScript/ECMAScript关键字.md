

Reserved keywords as of ECMAScript 2015：
* break
* case
* catch
* class
* const
* continue
* debugger
* default
* delete
* do
* else
* export
* extends
* finally
* for
* function
* if
* import
* in
* instanceof
* new
* return
* super
* switch
* this
* throw
* try
* typeof
* var
* void
* while
* with
* yield

from????

# this、super

this固定，不再善变

this关键字总是指向函数所在的当前对象

super关键字，指向当前对象的原型对象。


# import、export

## import




## export

[es6 export的几种写法](https://blog.csdn.net/qq_41818857/article/details/115762412)

一个模块只能有一个默认输出，因此export default命令只能使用一次


export  { } 

export {name,age,say}



export default name



export与变量声明的简写方式

export var app = {
  write: write
}



# const、var、let

从上到下，先声明再使用



let解决变量提升现象  var


const声明一个只读的常量。一旦声明，常量的值就不能改变。

# class function 

JavaScript 使用 constructor 方法当作构造函数，而 java 采用类名作为构造函数。
JavaScript 同 java 一致，都使用 extends 来继承。


typeof
instanceof
extends


yield
return
continue
break
