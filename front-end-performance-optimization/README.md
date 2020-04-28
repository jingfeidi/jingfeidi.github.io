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
**fis3**<br>
[fis3](http://fis.baidu.com/fis3/docs/beginning/intro.html)&nbsp;&nbsp;[fis3的GitHub](https://github.com/fex-team/fis3)&nbsp;&nbsp;
[fis3要点](https://github.com/jingfeidi/jingfeidi.github.io/blob/master/front-end-performance-optimization/fis3/README.md)&nbsp;&nbsp;
[fis3流程图](https://upload-images.jianshu.io/upload_images/704129-b488c5f93b1b0eb5.png)<br>
[webpack中文网](https://www.webpackjs.com/concepts/)&nbsp;&nbsp;[webpack官网](https://webpack.github.io/)&nbsp;&nbsp;
[gulp](https://www.gulpjs.com.cn/docs/getting-started/quick-start/)<br>
## 图片相关的优化
### 不同格式图片常用的业务场景<br>
jpg有损压缩，压缩率高，不支持透明&nbsp;(如果png8能支持实际开发，文件大小会更小些)<br>
png支持透明，浏览器兼容好<br>
webp压缩程度更好，在ios webview有兼容性问题，但在安卓中支持比较好 <br>
svg矢量图，代码内嵌，相对较小，图片样式相对简单的场景<br>
jpg —— 大部分不需要透明图片的业务场景<br>
png —— 大部分需要透明图片的业务场景<br>
webp —— 安卓全部<br>
svg矢量图 —— 图片样式相对简单的业务场景&nbsp;{logo，小的icon(用iconfont)}<br>
### 图片压缩几种方法
图片压缩：针对真实图片情况，舍弃一些相对无关紧要的色彩信息<br>
#### CSS雪碧图<br>
把你的网站上用到的一些图片整合到一张单独的图片中（PC端用得多些）<br>
优点：减少你的网站的HTTP请求数量<br>
缺点：整合图片比较大时，一次加载比较慢。可能这张图片非常大，如果这张图片在我们加载的过程中，没有正常加载进来的话，会导致整个页面都失去图片信息。<br>
将业务相关的整合到一个雪碧图里；将雪碧图拆分成多个，避免一个雪碧图特别大。

#### Image inline
将图片的内容内嵌到html当中&nbsp;(base64的方式)<br>
减少你的网站的HTTP请求数量
#### 使用矢量图
使用SVG进行矢量图的绘制<br>
使用iconfont解决icon问题  
#### 在安卓下使用webp
WebP 的优势体现在它具有更优的图像数据压缩算法，能带来更小的图片体积，而且拥有肉眼识别无差异的图像质量；同时具备了无损和有损的压缩模式、Alpha 透明以及动画的特性，在 JPEG 和 PNG 上的转化效果都非常优秀、稳定和统一。<br>

https://www.iconfont.cn/<br>
https://tinypng.com/ png压缩<br>

## css、js的加载与执行
## 懒加载与预加载
## 重绘与回流
## 浏览器存储
## 缓存
## 服务端性能优化
