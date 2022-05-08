
# 

下载：[Node.js 下载](https://nodejs.org/zh-cn/download/)

> 以下配置仅适用于 Windows 10


参考链接：  
[Nodejs安装及环境配置](https://segmentfault.com/a/1190000018634077)  
[Node.js下载安装以及配置NPM](https://www.jianshu.com/p/96f2f01a4f3e)

# 

NPM的全称是Node Package Manager，是一个NodeJS包管理和分发工具。它可以让 Javascript开发者能够更加轻松的共享代码和共用代码片段，并且通过 npm 管理你分享的代码也很方便快捷和简单。当需要用到别人的Javascript代码时可以直接通过npm安装，此时npm会根据依赖关系，把所有依赖的包都下载下来并且管理起来


```
PS C:\Users\mxs> node -v
v14.17.3
PS C:\Users\mxs> npm -v
6.14.13
PS C:\Users\mxs> npm root -g
D:\Tools_Dev\node-v14.17.3-win-x64\node_modules
PS C:\Users\mxs> npm install -g cnpm --registry=https://registry.npm.taobao.org
npm WARN deprecated request@2.88.2: request has been deprecated, see https://github.com/request/request/issues/3142
npm WARN deprecated har-validator@5.1.5: this library is no longer supported
D:\Tools_Dev\node-v14.17.3-win-x64\cnpm -> D:\Tools_Dev\node-v14.17.3-win-x64\node_modules\cnpm\bin\cnpm
+ cnpm@7.0.0
added 708 packages from 968 contributors in 45.612s
PS C:\Users\mxs> npm install @vue/cli -g
npm WARN deprecated @hapi/joi@15.1.1: Switch to 'npm install joi'
npm WARN deprecated request@2.88.2: request has been deprecated, see https://github.com/request/request/issues/3142
npm WARN deprecated @hapi/topo@3.1.6: This version has been deprecated and is no longer supported or maintained
npm WARN deprecated @hapi/bourne@1.3.2: This version has been deprecated and is no longer supported or maintained
npm WARN deprecated @hapi/address@2.1.4: Moved to 'npm install @sideway/address'
npm WARN deprecated @hapi/hoek@8.5.1: This version has been deprecated and is no longer supported or maintained
npm WARN deprecated har-validator@5.1.5: this library is no longer supported
npm WARN deprecated uuid@3.4.0: Please upgrade  to version 7 or higher.  Older versions may use Math.random() in certain circumstances, which is known to be problematic.  See https://v8.dev/blog/math-random for details.
npm ERR! cb() never called!

npm ERR! This is an error with npm itself. Please report this error at:
npm ERR!     <https://npm.community>

npm ERR! A complete log of this run can be found in:
npm ERR!     C:\Users\mxs\AppData\Roaming\npm-cache\_logs\2021-07-13T12_14_59_237Z-debug.log
PS C:\Users\mxs>
```

```cmd
PS C:\Users\mxs> npm config get cache
C:\Users\mxs\AppData\Roaming\npm-cache
PS C:\Users\mxs> npm config get prefix
D:\Tools_Dev\node-v14.17.3-win-x64
PS C:\Users\mxs>
```

```cmd
PS C:\Users\mxs> npm config get prefix
D:\Tools_Dev\nodejs
PS C:\Users\mxs> npm config get cache
C:\Users\mxs\AppData\Roaming\npm-cache
PS C:\Users\mxs> npm config set prefix "D:\Program Files\npm-global"
PS C:\Users\mxs> npm config get prefix
D:\Program Files\npm-global
PS C:\Users\mxs> npm config set prefix "D:\Tools_Dev\nodejs\npm-global"
PS C:\Users\mxs> npm config get prefix
D:\Tools_Dev\nodejs\npm-global
PS C:\Users\mxs> npm config set cache "D:\Tools_Dev\nodejs\npm-cache"
PS C:\Users\mxs> npm config get cache
D:\Tools_Dev\nodejs\npm-cache
PS C:\Users\mxs> npm install -g cnpm --registry=https://registry.npm.taobao.org
npm WARN deprecated request@2.88.2: request has been deprecated, see https://github.com/request/request/issues/3142
npm WARN deprecated har-validator@5.1.5: this library is no longer supported
D:\Tools_Dev\nodejs\npm-global\cnpm -> D:\Tools_Dev\nodejs\npm-global\node_modules\cnpm\bin\cnpm
+ cnpm@7.0.0
added 708 packages from 968 contributors in 27.655s
PS C:\Users\mxs> 
```

```cmd
PS C:\Users\mxs> npm config set registry https://registry.npm.taobao.org/
PS C:\Users\mxs> npm config get registry
https://registry.npm.taobao.org/
PS C:\Users\mxs>
```

```cmd
PS C:\Users\mxs> npm help

Usage: npm <command>

where <command> is one of:
    access, adduser, audit, bin, bugs, c, cache, ci, cit,
    clean-install, clean-install-test, completion, config,
    create, ddp, dedupe, deprecate, dist-tag, docs, doctor,
    edit, explore, fund, get, help, help-search, hook, i, init,
    install, install-ci-test, install-test, it, link, list, ln,
    login, logout, ls, org, outdated, owner, pack, ping, prefix,
    profile, prune, publish, rb, rebuild, repo, restart, root,
    run, run-script, s, se, search, set, shrinkwrap, star,
    stars, start, stop, t, team, test, token, tst, un,
    uninstall, unpublish, unstar, up, update, v, version, view,
    whoami

npm <command> -h  quick help on <command>
npm -l            display full usage info
npm help <term>   search for help on <term>
npm help npm      involved overview

Specify configs in the ini-formatted file:
    C:\Users\mxs\.npmrc
or on the command line via: npm <command> --key value
Config info can be viewed via: npm help config

npm@6.14.13 D:\Tools_Dev\nodejs\node_modules\npm
PS C:\Users\mxs>
```
```cmd

```
```cmd

```
```cmd

```
```cmd

```


# 安装 ZIP 版本

的默认存放路径位 C:\Users\用户名\AppData\Roaming\npm\node_modules下，可以通过CMD指令npm root -g查看


如果下载的是zip版本，则解压到哪个位置，就将解压缩后的目录添加到环境变量即可。npm全局包的默认位置就是 无需再配置npm全局包的下载目录，


删除时仅需删除安装包并移除环境变量即可

# 安装 MSI 版本

删除时需要到控制面板删除