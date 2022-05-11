


# 变量


ES6的新语法,叫做 解构

```
const { printName } = logger
```
等于
```
const printName = logger.printName;
```



```js
//Student.js
var student = {
    name: "mxs",
    age: 13
}

export { student }
```

```js
//index.js
import {student} from './Student.js';

const {name,age} = student;

console.log(name);
console.log(age);
```

```js
//index.js
import {student} from './Student.js';

const name = student.name;
const age = student.age;

console.log(name);
console.log(age);
```

定义的变量名必须是等号右边的对象中有的。


# 函数


## 参数传递
函数和对象作为参数


# class

class不存在变量提升,需要先定义再使用,因为ES6不会把类的声明提升到代码头部,但是ES5就不一样,ES5存在变量提升,可以先使用,然后再定义。

作用域

构造方法


---
类中定义属性（propertiy）：

```js
state = {
    departmentVo: {},
    visible: false,
};
```

---
类中定义方法（method）：


注意,定义“类”的方法的时候,前面不需要加上function这个关键字,直接把函数定义放进去了就可以了。另外,方法之间不需要逗号分隔,加了会报错。



```js
import * as React from 'react';
 
const { PureComponent, Fragment } = React;
 
class Test extends PureComponent {
    render() {
        return (
            <Fragment>
                <button>click</button>
                <button>click2</button>
            </Fragment>
        );
    }
    // 方式一，常规定义方式
    doClick() {
        console.log(this);
    }
    // 方式二，箭头函数定义方式
    doClick2 = () => {
        console.log(this);
    }
}
 
export default Test
```


render方法是

