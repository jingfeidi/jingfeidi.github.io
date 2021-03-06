# WEB经典面试题
边整理边默背记忆
## HTML5和CSS3基础
### 1. HTML5 基础
1.1. 请描述一个网页从开始请求到最终显示的完整过程？
一个网页从请求到最终显示的完整过程一般可分为如下 7 个步骤：
1. 在浏览器中输入网址；
2. 发送至 DNS 服务器并获得域名对应的 WEB 服务器的 IP 地址；
3. 与 WEB 服务器建立 TCP 连接；
4. 浏览器向 WEB 服务器的 IP 地址发送相应的 HTTP 请求；
5. WEB 服务器响应请求并返回指定 URL 的数据，或错误信息，如果设定重定向，则重定向到新的 URL 地址。
6. 浏览器下载数据后解析 HTML 源文件，解析的过程中实现对页面的排版，解析完成后在浏览器中显示基础页面。
7. 分析页面中的超链接并显示在当前页面，重复以上过程直至无超链接需要发送，完成全部显示。<br><br>
备注: [TCP百度百科](https://baike.baidu.com/item/TCP/33012?fr=aladdin)
TCP：传输控制协议（TCP，Transmission Control Protocol）是一种面向连接的、可靠的、基于字节流的传输层通信协议。TCP旨在适应支持多网络应用的分层协议层次结构。<br><br>

1.2. DOCTYPE 声明的作用是什么? 严格模式与混杂模式如何区分？<br>
HTML 语言已经存在太久了，目前必然会有一些不同版本的文档存在。为了能够让浏览器清楚你的文档的版本、类型和风格，需要在文档的起始用 DOCTYPE 声明指定当前文档的版本和风格。如果在网页中提供了版本信息，则可以有利于验证页面中的代码是否符合当前的版本和风格。<br>
*<!DOCTYPE>* 声明位于文档中的最前面，处于 <html> 标签之前，告知浏览器的解析器，用什么文档类型规范来解析这个文档。<br>
在严格模式（标准模式）中，浏览器根据规范呈现页面；在混杂模式中，页面以向后兼容的方式显示，以防止老站点无法工作。<br>
如果 HTML 文档包含形式完整的 DOCTYPE，那么它一般以标准模式呈现。对于 HTML4.01 文档，包含严格 DTD 的 DOCTYPE 常常导致页面以标准模式呈现。DOCTYPE 不存在或格式不正确会导致文档以混杂模式呈现。<br><br>

1.3. 简要描述常见的浏览器内核？<br>
浏览器内核负责对网页语法的解释并显示网页，它决定了浏览器如何显示网页的内容以及页面的格式信息。<br>
常见的浏览器内核有：<br>
Trident：IE 浏览器；<br>
Gecko：Mozilla 浏览器，比如 Firefox；<br>
Webkit：Safari 浏览器，也是 Chrome 浏览器的内核原型；<br>
Blink：Chrome 浏览器，Opera 浏览器。<br><br>

1.4. 如何理解 html 标签语义化？<br>
语义化的主要目的在于，直观的认识标签(markup)和属性(attribute)的用途和作用。可以概括为：用正确的标签做正确的事情。<br>
html 语义化可以让页面的内容结构化，便于浏览器解析，便于搜索引擎解析，并提高代码的可维护度和可重用性。<br>
比如，尽可能少的使用无语义的标签 div，使用结构化标签&lt;header&gt;、&lt;section&gt;、&lt;footer&gt;*。<br><br>

1.5. 锚点的作用是什么？如何创建锚点？<br>
锚点是文档中某行的一个记号，类似于书签，用于链接到文档中的某个位置。当定义了锚点后，我们可以创建直接跳至该锚点（比如页面中某个小节）的链接，这样使用者就无需不停地滚动页面来寻找他们需要的信息了。<br>
在使用 <a> 元素创建锚点时，需要使用 name 属性为其命名，代码如下所示：
```
<a name=”anchorname1”>锚点一</a>
```
然后就可以创建链接，直接跳转到锚点，代码如下所示：
```
<a href=”#anchorname1”>回到锚点一</a>
```

1.6. 使用 &lt;label&gt; 元素显示文本与使用其他文本标记显示文本有什么不同？<br>
&lt;label&gt;元素的直观效果是直接显示标记之间的文本，而且不会为文本呈现任何特殊效果。但是，它和其他文本标记所不同的是，它为鼠标用户改进了用户体验性。<br>
这是因为， &lt;label&gt; 元素可以附带一个 for 属性，只要将该属性的值设置为表单中任何一个控件的 id 属性的值，则当用户点击该标签（文本）时，浏览器就会自动将焦点转到和标签相关的表单控件上。即：如果在 &lt;label&gt;元素内点击文本，就会触发此控件。<br><br>

1.7. 列举常用的结构标记，并描述其作用。<br>
结构标记专门用于标识页面的不同结构，相对于使用&lt;div&gt; 元素而言，可以实现语义化的标签。<br>
常用的结构标记有：<br>
&lt;header&gt; 元素：用于定义文档的页眉；<br>
&lt;nav&gt; 元素：用于定义页面的导航链接部分；<br>
&lt;section&gt; 元素：用于定义文档中的节，表示文档中的一个具体的组成部分；<br>
&lt;article&gt; 元素：常用于定义独立于文档的其他部分的内容；<br>
&lt;footer&gt; 元素：常用于定义某区域的脚注信息；<br>
&lt;aside&gt; 元素：常用于定义页面的一些额外组成部分，如广告栏、侧边栏和相关引用信息等。<br>

1.8. 超级链接有哪些常见的表现形式？<br>
<a> 元素用于创建超级链接，常见的表现形式有：<br>
1、普通超级链接，语法为：
  ```
<a href="" target="">文本</a> 
  ```
2、下载链接，即目标文档为下载资源，语法如：
  ```
<a href="DAY02.zip">下载</a> 
  ```
3、电子邮件链接，用于链接到 email，语法如：
  ```
<a href="mailto:tarena@tarena.com.cn">联系我们</a> 
  ```
4、空链接，用于返回页面顶部，语法如：
  ```
<a href="#">...</a>
  ```
5、链接到 JavaScript，以实现特定的代码功能，语法如：
  ```
<a href="javascript : …">JS 功能</a> 
  ```

1.9. 简要描述行内元素和块级元素的区别。<br>
块级元素的前后都会自动换行，如同存在换行符一样。默认情况下，块级元素会独占一行。例如，&lt;p&gt;、&lt;hn&gt;、&lt;div&gt; 都是块级元素。在显示这些元素中间的文本时，都将从新行中开始显示，其后的内容也将在新行中显示。<br>
行内元素可以和其他行内元素位于同一行，在浏览器中显示时不会换行。例如，&lt;a&gt;、&lt;span&gt; 等。对于行内元素，不能设置其高度和宽度。<br>
还有一种元素，为行内块级元素，比如 &lt;img&gt; 、&lt;input&gt; 元素等。这些元素可以和其他行内元素位于同一行，同时可以设置其高度和宽度。<br><br>

1.10. 表单向服务器提交数据有几种方式？这些方式有什么区别？<br>
将表单数据发送给服务器的常用方式有两种：Get 和 Post。<br>
浏览器发送给服务器的 HTTP 请求分为请求头（header）和请求主体（body）两部分。其中，必须包含头部分，用于指定发送请求的方式、目的地以及其他关键信息；而主体是可选的。在头数据和主体数据之间用一个空白行来隔开。<br>
比如，需要发送请求到页面 GetStockPrice.php，且需要附带数据 Symbol=MSFT。那么如果使用 Get 方式发送数据，则简化后的请求数据内容如下所示：
```
GET /Trading/GetStockPrice.aspx?Symbol=MSFT HTTP/1.1
Host: localhost
```
如果使用 Post 方式发送数据，则简化后的请求数据内容如下所示：
```
POST /Trading/GetStockPrice.aspx HTTP/1.1
Host: localhost
Content-Type: application/x-www-form-urlencoded
Content-Length: 11
Symbol=MSFT
```
由此可见，两种方式的区别主要在于发送数据方式不同。<br>
使用 Get 方式向服务器发送表单数据时，表单数据将附加在 URL 属性的末端；采用POST 方法发送数据时，数据会放置在主体中发送。<br>

