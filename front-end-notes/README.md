# 基础问题解决方案
小技巧积累
## inline-block水平呈现的元素之间，换行显示或者空格分隔的情况下会有间距
**示例1：**<br>
参考网站：[li标签设置display:inline-block后产生的间距](https://www.cnblogs.com/qingjing/p/6579730.html)<br>
个人摘录小结：（非商用）<br>
给li标签添加diaplay:inline-block属性后，li标签并排显示后之间会产生3px的间距。<br>
![](https://images2015.cnblogs.com/blog/1122681/201703/1122681-20170319110439276-1122505397.png)
```
<style>
    ul,li{
        margin: 0;
        padding: 0;

    }
    li{
        display: inline-block;
        width: 50px;
        height:50px;
        background: black;
        list-style:none;
    }
</style>
<body>
    <ul>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
    </ul>
</body>
```
解决方法：<br>
1.li标签不换行；
```
<ul>
    <li></li><li></li><li></li><li></li>
 </ul>
```
2.使用HTML注释
```
<ul>
    <li></li><!--
    --><li></li><!--
    --><li></li><!--
    --><li></li>
</ul>
```
3.li标签左间距设置-3px；（不推荐）<br>
4.使用font-size:0（不推荐）<br>

