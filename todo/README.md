# 平常逛到的一些网站/网址
临时的，不定期更新整理

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
![](https://www.liudaima.com/zb_users/upload/2019/12/201912171576597404137597.png)
```
<body>
<header>header</header>
<main>main</main><aside>aside</aside>
<footer>footer</footer>
</body>
```

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
