# 平常逛到的一些网站/网址
临时的，不定期更新整理

## PV、UV、IV
[PV-百度百科](https://baike.baidu.com/item/%E7%BB%BC%E5%90%88%E6%B5%8F%E8%A7%88%E9%87%8F/396204?fromtitle=pv&fromid=402)&nbsp;&nbsp;[UV-百度百科](https://baike.baidu.com/item/%E7%8B%AC%E7%AB%8B%E8%AE%BF%E5%AE%A2/523828?fromtitle=UV&fromid=59745)&nbsp;&nbsp;[IV-百度百科](https://baike.baidu.com/item/iv/7919342#viewPageContent)<br><br>
**PV：**（page view，页面浏览量）一般指综合浏览量。是网站各网页被浏览的总次数。一个访客有可能创造十几个甚至更多的 Pageviews。是目前判断网站访问流量最常用的计算方式，也是反映一个网站受欢迎程度的重要指标之一。<br><br>
网页浏览数是评价网站流量最常用的指标之一，简称为PV。监测网站PV的变化趋势和分析其变化原因是很多站长定期要做的工作。 Page Views中的Page一般是指普通的html网页，也包含php、jsp等动态产生的html内容。来自浏览器的一次html内容请求会被看作一个PV，逐渐累计成为PV总数。<br><br>
除了PV总数外，还可以从不同角度来分析和对比PV，比如想知道哪个网页(Page)被浏览的次数多就要以Page为分析对象并分别累计PV。网页一般通过URL或标题(html title)来标识，大多数工具都提供了类似的定义方法]关于PV的统计要考虑2种特殊情况：<br>
一是从服务器返回错误网页或重定向网页时，是否计数以及如何配置；<br>二是本地或网关服务器的缓存生效时是否计数。<br>这些问题在实施网站分析前需要搞清楚，必要时可以咨询工具厂商。<br><br>

**UV：**（网站独立访客）一般指独立访客。独立（IP）访客。相当于网络中访客的IP地址。依据浏览器的“cookie” 判定。<br><br>
一般地，我们可以用两个数值标准来统计访问某网站的访客，即“访问次数”和“独立访客（问）数”，访问次数和独立访客数是两个不同的概念。<br>
访问次数，相当于一个展览会的访问人次(次数)，相当于网络中的PV值。<br>独立访客数，相当于带身份证参观展览会的访问人数，每一个出示身份证参观展览的人，无论出入几次，都只计作一次独立访问。这里所说的“身份证”，在网络上就是访客的IP地址或Cookie。<br><br>
**UV技术依据：** 网站统计工具对于网站独立访客数的计算，主要是依据浏览器的“cookie” 来判定的。在浏览器cookie数据不清除的情况下，即使用多个IP切换来登录一个网站，也会只记为一个访客数。<br><br>
独立访客很接近但并不完全就是真实独立的人。其次，独立访客这个指标会受浏览器设置的影响，如那些将浏览器设置成禁用cookie或是禁用第三方cookie的情况。大多数的网站分析工具都使用第一方cookie来尽量降低cookie被禁用的情况(被禁用百分比大概在2%至5%之间)。第三方cookie被禁用的比率相对而言就要高很多(大概在10%至30%之间)。<br><br>
具有统计功能的统计系统，可以根据其他条件判断出实际使用的用户数量，返回给网站建设者真实、可信和准确的信息。比如通过注册的用户，甚至可以区分出网吧、机房等共享一个ip地址的不同计算机。<br><br>
**计算规则：**
记录独立访客数的时间标准一般可为一天，一个月。按照国际惯例，独立访客数记录标准一般为“一天”，即一天内如果某访客从同一个IP地址来访问某网站n次的话，访问次数计作n, 独立访客数则计作1。一般不计算年UV数。

## HTML相关
[HTML &lt;main&gt;标签](https://www.w3school.com.cn/tags/tag_main.asp)<br>
&lt;main&gt; 标签规定文档的主要内容。<br>
&lt;main&gt;元素中的内容对于文档来说应当是唯一的。它不应包含在文档中重复出现的内容，比如侧栏、导航栏、版权信息、站点标志或搜索表单。<br>
注释：在一个文档中，不能出现一个以上的 &lt;main&gt; 元素。&lt;main&gt;元素不能是以下元素的后代：&lt;article&gt;、&lt;aside&gt;、&lt;footer&gt;、&lt;header&gt; 或 &lt;nav&gt;。<br>
[html5 main标签是什么意思？html5 main标签作用的详细介绍](https://www.php.cn/html5-tutorial-408543.html)<br>
[HTML &lt;main&gt;标签蚂蚁部落](https://www.softwhy.com/article-10285-1.html)<br>
[HTML Demo:  &lt;main&gt;&nbsp;MDN](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/main)<br>
[HTML5标签：aside元素的使用方法及作用](https://www.liudaima.com/a/174.html)<br>
[HTML5标签：article元素的使用方法及作用](https://www.liudaima.com/a/173.html)<br>
[H5标签在IE浏览器下的兼容性问题](https://blog.csdn.net/Hi_Riley/article/details/89220739)&nbsp;例子讲的主要是main标签<br>
**小结：**
由header、main、aside、footer 四个标签组成的经典布局如下图：<br>
![](https://github.com/jingfeidi/jingfeidi.github.io/blob/master/front-end-notes/img/201912171576597404137597.png)
```
<body>
<header>header</header>
<main>main</main><aside>aside</aside>
<footer>footer</footer>
</body>
```
以上代码中，main标签还可以使用article标签替换。<br><br>
**HTML &lt;main&gt;标签**<br>
&lt;main&gt;标签规定文档主要内容或应用程序的主体部分；<br>
&lt;main&gt;标签是 HTML5中新增的标签；<br>
&lt;main&gt;标签只能在整个页面中最多出现一次；<br>
&lt;main&gt;标签不能是以下标签的子标签：&lt;article&gt;、&lt;aside&gt;、&lt;footer&gt;、&lt;header&gt; 或 &lt;nav&gt;。<br>
&lt;main&gt;标签中的主体内容应该是页面中唯一的，且不会在其他页面中重复出现的内容。它不应包含在文档中重复出现的内容，比如侧栏、导航栏、版权信息、站点标志或搜索表单；<br><br>
**使用 &lt;main&gt;元素最简单的方式就是去替换那些 ID 或者 Class 值为 main 或者 content 之类的 &lt;div&gt;元素：**<br>
使用 &lt;main&gt;元素之前的文档结构：
```
<header>Header</header>
<div id="content">Main Content</div>
<footer>Footer</footer>
```  
使用&lt;main&gt;元素改写文档：
```
<header>Header</header>
<main id="content">Main Content</main>
<footer>Footer</footer>  
```
**&lt;main&gt;标签的兼容性问题：**<br>
1. IE9中的问题：<br>
IE9浏览器会将H5部分语义化标签，解析为行内元素，比如：main标签。<br>
解决办法：给main标签设置display：block样式
```
main {display:block;}
```
2. IE8及以下的问题：<br>
IE8及以下浏览器根本不认识H5标签<br>
解决办法：<br>
2.1 利用js手动创建标签，比如：document.createElement(‘main’)，创建的标签默认为行内元素，因此需要给标签样式设置display：block；
```
<script type="text/javascript">document.createElement('main');</script>
```
2.2 利用第三方插件：html5shiv.min.js，直接引入即可

## head
```
<meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1">
```
兼容性配置，让IE走最高的浏览器edge去渲染，如果有chrome浏览器用chrome去渲染<br>
```
<meta name="renderer" content="webkit">
```
让双核浏览器优先使用webkit内核渲染页面

## md格式的文档编写相关
[如何写md格式的文档](https://www.jianshu.com/p/f378e3f2e7e1)<br>
[markdown添加空格缩进[全]](https://blog.csdn.net/zdx1996/article/details/86590864)

## 前端动画技术
[前端动画技术的研究和比较](https://segmentfault.com/a/1190000015360884)<br>
[原生 JS 实现帧动画库](https://www.imooc.com/learn/659)<br>
[jQuery基础(四)—动画篇](https://www.imooc.com/learn/430)<br>
[JS动画效果](https://www.imooc.com/learn/167)<br>
[CSS动画实用技巧](https://www.imooc.com/learn/357)<br>
[带你走入前端动画的世界](https://www.imooc.com/learn/1190)<br>
[使用Web Animations API创建炫酷动画](https://www.jianshu.com/p/dbc5452c1898)<br>
[window.requestAnimationFrame](https://developer.mozilla.org/zh-CN/docs/Web/API/Window/requestAnimationFrame)<br>
[CSS3动画那么强，requestAnimationFrame还有毛线用？](https://www.zhangxinxu.com/wordpress/2013/09/css3-animation-requestanimationframe-tween-%e5%8a%a8%e7%94%bb%e7%ae%97%e6%b3%95/)<br>
[js动画api - requestAnimationFrame](https://blog.csdn.net/u013282116/article/details/69260764)

## GPU加速
[GPU 加速是什么](http://www.sohu.com/a/133467734_114877)<br>
[使用CSS3开启GPU硬件加速提升网站动画渲染性能](https://blog.csdn.net/hsany330/article/details/50925260)<br>
[CSS3 GPU硬件加速](https://www.cnblogs.com/mengfangui/p/6604577.html)<br>
[17.CSS3如何开启GPU加速](https://www.jianshu.com/p/769c4682ff00)

## 如何捕获js异常
[window.onerror的总结](https://www.jianshu.com/p/315ffe6797b8)<br>

## 词
[UWP百度百科](https://baike.baidu.com/item/Universal%20Windows%20Platform/23796796?fromtitle=uwp&fromid=4236943&fr=aladdin)<br>
1.UWP即Windows 10中的Universal Windows Platform简称。<br>2.即Windows通用应用平台，在Windows 10 Mobile/Surface（Windows平板电脑）/PC/Xbox/HoloLens等平台上运行，uwp不同于传统pc上的exe应用，也跟只适用于手机端的app有本质区别。<br>3.它并不是为某一个终端而设计，而是可以在所有Windows10设备上运行。<br>

## 谷歌浏览器
Sources：看源代码<br>Elements：调试DOM元素<br>Network：网络加载(加载顺序、时长)<br>Console：来报错<br>Performance：性能<br>Memory：与内存相关的<br>Application：整个网站应用<br>Security：安全<br>Audits：也可以看一些性能
