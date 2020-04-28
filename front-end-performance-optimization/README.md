# 前端性能优化
浏览器请求过程中一些潜在的性能优化点<br>
1. dns是否可以通过缓存减少dns查询时间？<br>
2. 网络请求的过程走最近的网络环境？<br>
3. 相同的静态资源是否可以缓存？<br>
4. 能否减少请求http请求大小？<br>
5. 减少http请求<br>
6. 服务端渲染<br>

## 资源合并与压缩
减少http请求数量、减少请求资源的大小<br>
### 1. html压缩
压缩那些在文本文件中有意义，但是在HTML中不显示的字符，包括空格，制表符，换行符等，还有一些其他意义的字符，如HTML注释也可以被压缩。
### 2. css压缩
无效代码删除、css语义合并
### 3. Js压缩与混乱
无效字符的删除、剔除注释、代码语义的缩减和优化、代码保护
### 4.文件合并
**不合并文件存在的一些问题**<br>
文件与文件之间有插入的上行请求，增加了N-1个网络延迟<br>
受丢包问题影响更严重<br>
经过代理服务器时可能会被断开<br><br>
**文件合并存在的问题**<br>
首屏渲染问题、缓存失效问题<br>
解决：<br>
1. 对公共库进行合并<br>
公共库单独打包一个文件，将业务代码单独打包一个文件，改业务代码时不会影响到公共库缓存的情况<br>
2. 不同页面的合并<br>
针对单页面应用程序，一开始页面渲染的时候它会请求当前页面所对应的js，而不是将整个单页面应用所有的js都打成一个包直接请求回来。<br>
实际做的过程中，当前端路由到单页面某个页面的时候，我们才去加载那个页面的组件，才去加载那个页面所对应的js文件。这样就是将不同页面的js进行分别打包。这种方式在webpack中可以实现。<br>
3. 随机应变，怎么合适怎么来<br>
### 如何进行文件合并
使用构建工具gulp、fis3、webpack等进行文件合并<br>
构建工具网址<br>
**fis3**
[fis3](http://fis.baidu.com/fis3/docs/beginning/intro.html)&nbsp;&nbsp;[fis3的GitHub](https://github.com/fex-team/fis3)&nbsp;&nbsp;
[fis3要点](https://github.com/jingfeidi/jingfeidi.github.io/blob/master/front-end-performance-optimization/fis3/README.md)<br>
[webpack中文网](https://www.webpackjs.com/concepts/)&nbsp;&nbsp;[webpack官网](https://webpack.github.io/)&nbsp;&nbsp;
[gulp](https://www.gulpjs.com.cn/docs/getting-started/quick-start/)<br>
[fis3流程图](https://upload-images.jianshu.io/upload_images/704129-b488c5f93b1b0eb5.png)<br>
## 图片相关的优化
## css、js的加载与执行
## 懒加载与预加载
## 重绘与回流
## 浏览器存储
## 缓存
## 服务端性能优化
