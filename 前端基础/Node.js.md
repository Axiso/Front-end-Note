
# Node.js

Node.js 是一个基于 Chrome V8 引擎 的 JavaScript 运行时。  

相关链接：  
[Node.js 官网](https://nodejs.org/zh-cn/)  
[vscode 使用 nodejs](https://code.visualstudio.com/docs/nodejs/working-with-javascript)

# 模块安装

项目目录下执行mpm安装命令安装nodjs模块时，默认安装的位置是在项目的根目录下新建一个node_modules文件夹，然后安装到node_modules目录下。

# 

this 在nodejs环境下默认为空对象，在浏览器环境下默认为Windows对象。  

<img src="../pic/JavaScript/this2.png" width="80%" >
<img src="../pic/JavaScript/this1.png" width="80%" >





# 问题总结

```
PS D:\code\renren-fast-vue-master> node -v
v10.14.2
PS D:\code\renren-fast-vue-master> npm run dev

> renren-fast-vue@1.2.2 dev D:\code\renren-fast-vue-master
> webpack-dev-server --inline --progress --config build/webpack.dev.conf.js

[webpack-cli] Error: Unknown option '--inline'
[webpack-cli] Run 'webpack --help' to see available commands and options
npm ERR! code ELIFECYCLE
npm ERR! errno 2
npm ERR! renren-fast-vue@1.2.2 dev: `webpack-dev-server --inline --progress --config build/webpack.dev.conf.js`
npm ERR! Exit status 2
npm ERR!
npm ERR! Failed at the renren-fast-vue@1.2.2 dev script.
npm ERR! This is probably not a problem with npm. There is likely additional logging output above.

npm ERR! A complete log of this run can be found in:
npm ERR!     C:\Users\Administrator\AppData\Roaming\npm-cache\_logs\2021-10-12T11_44_01_024Z-debug.log
PS D:\code\renren-fast-vue-master>
```

解决方法：
```
cnpm install webpack-dev-server@2.9.7
```
