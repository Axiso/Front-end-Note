浏览器对象模型

可以类似理解为操作系统的接口

console.log()是js的

window.alert()
window.onload()就是浏览器的


## 

windows窗口有六大子模块：
document
history
location
screen
navigator
frame HTML

可以省略window


document.body.offsetWidth
document.body.offsetHeight

1. window.screen 对象  
window.screen 对象包含用户屏幕的信息。  
* screen.width  
* screen.height  
* screen.availWidth  
* screen.availHeight  
* screen.colorDepth  
* screen.pixelDepth  
---
2. window.location 对象  
window.location 对象可用于获取当前页面地址（URL）并把浏览器重定向到新页面。  
* location.href 返回当前页面的 href (URL)
* location.hostname 返回 web 主机的域名
* location.pathname 返回当前页面的路径或文件名
* location.protocol 返回使用的 web 协议（http: 或 https:）
* location.assign 加载新文档
  
  JavaScript 有三种类型的弹出框：警告框、确认框和提示框。  
* window.alert()  alert()  
* window.confirm()  confirm()  
* window.prompt()  prompt()  
---
1. window.history 对象  
window.history 对象包含浏览器历史。
* history.back() - 等同于在浏览器点击后退按钮
* history.forward() - 等同于在浏览器中点击前进按钮  
想要在浏览器左上角看到前进和后退的效果，必须存在路径的跳转。
---


setTimeout(function, milliseconds)
在等待指定的毫秒数后执行函数。
setInterval(function, milliseconds)
等同于 setTimeout()，但持续重复执行该函数。
clearTimeout() 方法停止执行 setTimeout() 中规定的函数。
clearInterval() 方法停止 setInterval() 方法中指定的函数的执行。




