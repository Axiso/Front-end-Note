
# 
API 是已经建立好的一套代码组件，可以让开发者实现原本很难甚至无法实现的程序。就像现成的家具套件之于家居建设，用一些已经切好的木板组装一个书柜，显然比自己设计，寻找合适的木材，裁切至合适的尺寸和形状，找到正确尺寸的螺钉，再组装成书柜要简单得多。

JavaScript 语言核心之上所构建的功能更令人兴奋。应用程序接口（Application Programming Interfaces（API））将为你的代码提供额外的超能力。

<img src="../pic/JavaScript/browser.png" width="80%" >


API 通常分为两类。
* 浏览器 API  
  浏览器 API 内建于 web 浏览器中，它们可以将数据从周边计算机环境中筛选出来，还可以做实用的复杂工作。例如：
    * 文档对象模型 API（DOM（Document Object Model）API） 能通过创建、移除和修改 HTML，为页面动态应用新样式等手段来操作 HTML 和 CSS。比如当某个页面出现了一个弹窗，或者显示了一些新内容（像上文小 demo 中看到那样），这就是 DOM 在运行。
    * 地理位置 API（Geolocation API） 获取地理信息。这就是为什么 谷歌地图 可以找到你的位置，而且标示在地图上。
    * 画布（Canvas） 和 WebGL API 可以创建生动的 2D 和 3D 图像。人们正运用这些 web 技术制作令人惊叹的作品。参见 Chrome Experiments 以及 webglsamples。
    * 诸如 HTMLMediaElement 和 WebRTC 等 影音类 API 让你可以利用多媒体做一些非常有趣的事，比如在网页中直接播放音乐和影片，或用自己的网络摄像头获取录像，然后在其他人的电脑上展示（试用简易版 截图 demo 以理解这个概念）。

* 第三方 API  
  第三方 API 并没有默认嵌入浏览器中，一般要从网上取得它们的代码和信息。比如：
    * Twitter API、新浪微博 API 可以在网站上展示最新推文之类。
    * 谷歌地图 API、高德地图 API 可以在网站嵌入定制的地图等等。