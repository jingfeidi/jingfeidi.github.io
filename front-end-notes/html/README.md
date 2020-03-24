# HTML相关知识
## HTML语义化


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
让双核浏览器优先使用webkit内核渲染页面<br>

```
<link rel="dns-prefetch" href="//s1.hdslb.com">
```
DNS预解析，在页面的html标签中添加dns-prefetch告诉浏览器对指定域名预解析。当前域名是bilibili.com，而指定域名是s1.hdslb.com。DNS预解析dns-prefetch提升页面载入速度优化前端性能。

