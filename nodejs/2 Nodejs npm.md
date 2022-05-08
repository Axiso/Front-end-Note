# npm


> npm类似于maven；  
> package.json类似于pom.xml。


# nodejs和npm的关系



# 全局安装与本地安装
npm 的包安装分为本地安装（local）、全局安装（global）两种，从敲的命令行来看，差别只是有没有-g而已，比如

```
npm install express          # 本地安装
npm install express -g   # 全局安装
```

> 如果出现以下错误：
> ```
> npm err! Error: connect ECONNREFUSED 127.0.0.1:8087 
> ```
> 解决办法为：
> ```
> $ npm config set proxy null
> ```
## 本地安装
1. 将安装包放在 ./node_modules 下（运行 npm 命令时所在的目录），如果没有 node_modules 目录，会在当前执行 npm 命令的目录下生成 node_modules 目录。
2. 可以通过 require() 来引入本地安装的包。

## 全局安装
1. 将安装包放在 /usr/local 下或者你 node 的安装目录。
2. 可以直接在命令行里使用。

如果你希望具备两者功能，则需要在两个地方安装它或使用 npm link。

接下来我们使用全局方式安装 express
```
$ npm install express -g
```
安装过程输出如下内容，第一行输出了模块的版本号及安装位置。
```
express@4.13.3 node_modules/express
├── escape-html@1.0.2
├── range-parser@1.0.2
├── merge-descriptors@1.0.0
├── array-flatten@1.1.1
├── cookie@0.1.3
├── utils-merge@1.0.0
├── parseurl@1.3.0
├── cookie-signature@1.0.6
├── methods@1.1.1
├── fresh@0.3.0
├── vary@1.0.1
├── path-to-regexp@0.1.7
├── content-type@1.0.1
├── etag@1.7.0
├── serve-static@1.10.0
├── content-disposition@0.5.0
├── depd@1.0.1
├── qs@4.0.0
├── finalhandler@0.4.0 (unpipe@1.0.0)
├── on-finished@2.3.0 (ee-first@1.1.1)
├── proxy-addr@1.0.8 (forwarded@0.1.0, ipaddr.js@1.0.1)
├── debug@2.2.0 (ms@0.7.1)
├── type-is@1.6.8 (media-typer@0.3.0, mime-types@2.1.6)
├── accepts@1.2.12 (negotiator@0.5.3, mime-types@2.1.6)
└── send@0.13.0 (destroy@1.0.3, statuses@1.2.1, ms@0.7.1, mime@1.3.4, http-errors@1.3.1)
```


# package.json和package-lock.json

package-lock.json
package.json 位于模块的目录下，用于定义包的属性。



package.json类似于pom.xml


Node.js REPL(Read Eval Print Loop:交互式解释器) 表示一个电脑的环境，类似 Windows 系统的终端或 Unix/Linux shell，我们可以在终端中输入命令，并接收系统的响应。

package-lock.json的作用：

锁版本，确保项目在后续拉去中，安装依赖包时依赖包的版本始终是统一的

在npm install时会自动生成package-lock.json

package.json与package-lock.json相同时，npm安装包时以package-lock.json为准

package-lock.json与package.json的不同：

package-lock.json记录的是依赖树，记录了依赖模块之间的完整依赖关系。package.json记录的是依赖项，不能锁定依赖的依赖。

总结： package-lock.json 文件的作用锁定安装时的包的版本号，并且需要上传到 git，以保证其他人在 npm install 时大家的依赖能保证一致。


## package.json

devDependencies和dependencies

peerDependencies

[一文搞懂peerDependencies](https://segmentfault.com/a/1190000022435060)

# npm命令

## 安装
```
npm install
```

会下载项目根目录下 package.json 文件中指定的依赖到 `./node_modules` 目录下。

在本地目录中如果没有 package.json 这个文件的话，那么最新版本的包会被安装。

如果存在 package.json 文件，则会在 package.json 文件中查找针对这个包所约定的语义化版本规则，然后安装符合此规则的最新版本。


在不同的电脑上执行该命令，即使项目代码相同，但由于nodejs环境不同也会报错。
```
PS D:\IntelliJ IDEA\ly-ui-scaffold\src> npm install
npm ERR! code ERESOLVE
npm ERR! ERESOLVE unable to resolve dependency tree
npm ERR!
npm ERR! While resolving: ly-ui-scaffold@3.0.0
npm ERR! Found: react@16.14.0
npm ERR! node_modules/react
npm ERR!   react@"^16.6.3" from the root project
npm ERR!   peer react@">=16.0.0" from antd@3.26.20
npm ERR!   node_modules/antd
npm ERR!     antd@"^3.10.9" from the root project
npm ERR!
npm ERR! Could not resolve dependency:
npm ERR! peer react@"^18.1.0" from react-dom@18.1.0
npm ERR! node_modules/react-dom
npm ERR!   peer react-dom@">=16.0.0" from antd@3.26.20
npm ERR!   node_modules/antd
npm ERR!     antd@"^3.10.9" from the root project
npm ERR!
npm ERR! Fix the upstream dependency conflict, or retry
npm ERR! this command with --force, or --legacy-peer-deps
npm ERR! to accept an incorrect (and potentially broken) dependency resolution.
npm ERR!
npm ERR! See C:\Users\admin\AppData\Local\npm-cache\eresolve-report.txt for a full report.

npm ERR! A complete log of this run can be found in:
npm ERR!     C:\Users\admin\AppData\Local\npm-cache\_logs\2022-05-07T01_39_10_612Z-debug-0.log
PS D:\IntelliJ IDEA\ly-ui-scaffold\src> 
```

在新版本的npm（v7）中，默认情况下，npm install当遇到冲突的peerDependencies时将失败。不会继续安装，并提示：

```
Fix the upstream dependency conflict, or retry
this command with --force, or --legacy-peer-deps
to accept an incorrect (and potentially broken) dependency resolution.
```
这样的关键字，这是npm版本的依赖冲突的提示使然，
那么npm：何时使用--force和--legacy-peer-deps？
--force 会无视冲突，并强制获取远端npm库资源，即使本地有资源也会覆盖掉
--legacy-peer-deps：安装时忽略所有peerDependencies，忽视依赖冲突，采用npm版本4到版本6的样式去安装依赖，已有的依赖不会覆盖，。

```
npm install --legacy-peer-deps
```


## 运行
```
npm run
```

## 启动
```
npm start
```



```
PS D:\IntelliJ IDEA\ly-ui-scaffold\src> npm start

> ly-ui-scaffold@3.0.0 start
> cross-env APP_TYPE=site umi dev

🚀 Starting Umi UI using umi@3.5.23...
🌈 Umi UI mini Ready on port 3000.
Starting the development server...

√ Webpack
  Compiled successfully in 1.31m

 DONE  Compiled successfully in 78696ms                                                    10:00:39

  App running at:
  - Local:   http://localhost:8012 (copied to clipboard)
  - Network: http://192.168.6.29:8012

启动时间有点慢，试试新出的 MFSU 方案，1s+ 完成启动，详见 https://github.com/umijs/umi/issues/6766  
 WAIT  Compiling...                                                                        10:00:40

√ Webpack
  Compiled successfully in 2.10s

 DONE  Compiled successfully in 2095ms                                                     10:00:42

```