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
将图片的内容内嵌到html当中&nbsp;(base64的方式，webp格式)<br>
减少你的网站的HTTP请求数量
#### 使用矢量图
使用SVG进行矢量图的绘制<br>
使用iconfont解决icon问题  
#### 在安卓下使用webp
WebP 的优势体现在它具有更优的图像数据压缩算法，能带来更小的图片体积，而且拥有肉眼识别无差异的图像质量；同时具备了无损和有损的压缩模式、Alpha 透明以及动画的特性，在 JPEG 和 PNG 上的转化效果都非常优秀、稳定和统一。<br>

https://www.iconfont.cn/<br>
https://tinypng.com/ &nbsp;png压缩<br>
https://zhitu.isux.us/ &nbsp;智图将jpg或png转为webp图片<br>
fis3 将jpg或png 转为webp图片<br>
```
fis.match('*.{jpg,png}', {
    rExt: '.webp',
    parser: fis.plugin('webp',{
        quality: 60
    })
})
```
小于8KB的图片，用 Image inline 来做<br><br>
**雪碧图制作**<br>
在PS里，将多个icon合成一张图<br>
雪碧图样式生成&nbsp; http://www.spritecow.com/ <br><br>
**SVG:**<br>
https://www.w3school.com.cn/svg/index.asp <br>
https://www.w3.org/Graphics/SVG/ <br>
Graphics：图形 <br>
https://www.w3.org/Graphics/SVG/WG/track/ <br>
## css、js的加载与执行
![](https://github.com/jingfeidi/jingfeidi.github.io/blob/master/front-end-performance-optimization/img/htmlrender.png)<br>
html页面加载渲染的过程<br>
### HTML渲染过程的一些特点
**顺序执行、并发加载**<br>
并发加载：html可能引入很多css/js等外部资源，这些外部资源在浏览器加载过程时并发加载的。并发加载过程，受浏览器域名限制，对单个域名，我们浏览器并发度是有限的，所以这时，我们经常(很多资源是托管在CDN上的)，设3到4个CDN域名，防止一个CDN域名未达到浏览器外部资源并发请求数目的上限，导致很多资源其实没有做到全部的并发请求。<br>
**是否阻塞**<br>
css加载是否阻塞之后的js加载<br>
css加载是否阻塞后续js执行<br>
css加载是否阻塞页面的渲染<br>
**依赖关系**<br>
html在渲染的过程中是否存在一定要遵循的依赖关系，保证依赖关系正确的情况下能提高我们的效率。<br>
比如：页面渲染出来了，但是我们css样式没有出来，突然闪了一下，页面的样式出来了，这种情况实际上在开发过程是常见的，css资源有可能加载慢的情况，会导致我们页面突然样式从没有到有，有一个突然闪过的过程。这种情况是没有遵循好依赖关系，如果我们把css代码放在head当中去引入的话，那么整个页面的渲染实际上会等待我们head中所引入的css加载并生成css树，最终成为Render Tree之后去进行页面的渲染，这个渲染的结果一定是带有样式的，这样就不会出现闪动bug。<br>
另：js执行顺序是否有依赖关系，有时候我们可以通过js标签上的async让js异步加载，不会阻塞DOM树我们页面的渲染，但是async实际上是放弃了相关js的依赖关系，哪个js先加载完，它就执行哪个。<br>
**引入方式**<br>
对CSS：link引入还是import引入，两种方式之间有什么区别，怎么引入更优。<br>
对JS：最基础的script src的方式去引入，会有相关阻塞页面渲染的问题；是否能通过defer、async去处理比较特殊的js引入；
js资源是否要通过动态引入方式，在任何我们需要js资源的时候才去异步加载。单页面应用，当路由到单页面某个页面时，才去加载那个页面所对应的js文件。<br><br>
**顺序执行、并发加载**<br>
词法分析：浏览器对html文档解析的方法它会从我们的html最开始的部分对我们tag进行从上到下的依次解析，去匹配从上到下的每个token，它的匹配顺序，词法顺序是从上到下，从而导致css资源js资源以及页面DOM树的生成都是从上到下的，这个从上到下的很多资源引入的时候可能会产生一些阻塞的情况。词法分析的token获取是从上到下的，从而导致我们整个html被解析的过程是从上到下的，所以整体的html是按顺序执行的。<br>
并发加载：html中所引入的外部资源是并发去请求的<br>
并发上限：某个域名下它的并发请求数是有个上限的，需要去控制某个域名下所请求的资源避免达到资源上限<br>
**css阻塞**<br>
css head中阻塞页面的渲染：避免页面的闪动，css在head中通过link的方式引入，会阻塞页面的渲染。阻塞页面的渲染的意思是这个页面要呈现出相应的效果就需要link所对应的css加载完之后它才会去进行渲染。css加载完并分析完了，它整个渲染是带样式的。推荐css在head中通过link的方式引入。<br>
css阻塞js的执行：css资源加载完之前，后续js执行它是会被阻塞的。因为js很有可能是要去操作DOM,涉及到css样式的修改，它这个修改实际上是依赖于我们之前引入的css所具有的样式的基础上去进行的。<br>
css不阻塞外部脚本的加载：css资源加载完之前，不阻塞后续js加载<br>
**js阻塞**<br>
直接引入的js阻塞页面的渲染：js代码可能修改文档结构，会阻塞后面节点的创建<br>
js不阻塞资源的加载：webkit增加了预先扫描器以及预资源加载器<br>
js顺序执行，阻塞后续js逻辑的执行：连续引入多个js，会顺序执行，单线程的。<br>
**依赖关系**<br>
页面渲染依赖于css的加载<br>
js的执行顺序的依赖关系<br>
js逻辑对于dom节点的依赖关系<br>
**加载和执行的一些优化点**<br>
css 样式表置顶（css在head中通过link的方式引入）<br>
用 link 代替 import<br>
js 脚本置底（还有不置底的方法待补充）<br>
合理使用 js 的异步加载能力<br><br>
使用 performance 工具分析网站页面的加载过程


## 懒加载与预加载
### 懒加载
图片进入可视区域之后请求图片资源<br>
对于电商等图片很多，页面很长的业务场景适用<br>
减少无效资源的加载<br>
并发加载的资源过多会阻塞js的加载，影响网站的正常使用<br>
淘宝网首页图片加载就是懒加载
### 预加载
图片等静态资源在使用之前的提前请求<br>
资源使用到时能从缓存中加载，提升用户体验<br>
页面展示的依赖关系维护<br>
抽奖页面图片加载，H5活动页图片加载都是预加载
## 重绘与回流
## 浏览器存储
## 缓存
## 服务端性能优化
