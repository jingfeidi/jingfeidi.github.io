# Atom软件（安装/插件/使用/快捷键/tips）
## 1.安装
https://github.com/atom/atom/releases/tag/v1.47.0<br>
从3个中选择你需要的进行下载：<br>
![](http://m.qpic.cn/psc?/V120flX00zHgB1/4YNML3SP3kohrZcOJ8e1uiZV5Di0WgQKpTPC7QbgX4ZKOiGuIKTCq3EGOWWGOApp2EaMgNwePA6uJyzP1tOT63zOJUMKvwmroOVEsZOLcnQ!/b&bo=JQNuAgAAAAADF3g!&rf=viewer_4)<br><br>
下载下来后，解压下载好的压缩包，将解压后的文件放在你想要的位置，将里面的Atom.exe鼠标右键发送到=>桌面快捷方式，就可以开始使用了。<br>
![](https://m.qpic.cn/psc?/V120flX00zHgB1/9XwfBMWIaa5Dh0kEemxh*Bfl064ptUbpVjQn7aRJuo7tIkJ7FPpcqfcfbV9xTki16fiKRkIIB7hem4ILZM0Sag!!/b&bo=WAPaAQAAAAADB6I!&rf=viewer_4)<br><br>
参考网站 [ATOM 编辑器安装使用](https://blog.csdn.net/qq_35275056/article/details/82598637)<br>

## 2.插件/使用
Atom 使用教程： <br>
 软件基础 https://wiki.jikexueyuan.com/project/atom/basis.html<br>
 插件主题推荐 https://wiki.jikexueyuan.com/project/atom/plug-in.html<br><br>
Atom的插件必备： https://www.jianshu.com/p/b779e2e5e3ef<br><br>
**启动界面 介绍**<br>
  **菜单栏-分为六大块:**<br>
    File — 文件的保存打开,项目的保存打开,最后一次的项目加载,关闭及设置中心, 以及用户自定义的配置(配置文件,初始化脚本,样式风格,代码片段,快捷键配置文件)等<br>
    Edit — 文件编辑的操作,文件编码格式,及行跳转等<br>
    View — 重载页面,全屏,字体大小的缩放等<br>
    Find — 都是关于查询的 ,跟 Sublime text 极其相似,快捷键基本一样<br>
    Package — 包,就是插件列表的集合点<br>
    Help — 帮助文档,软件更新,协议等<br><br>
    
**设置中心 File=>Settings**<br>
  左边侧栏-自上而下分为六大部分<br>
    Settings — 全局设置,可以设置文件的编码,菜单栏是否显示,忽略文件,文档缩进,字体大小,项目主目录等,这个比 sublime text 人性化,简洁明了的配置<br>
    Keybindings — 快捷键配置,默认快捷键都汇总于此了,很方便查询对应的快捷键的功能,也方便修改…人性化<br>
    Packages — 插件管理中心,可以设置插件,删除插件及禁用,无安装功能<br>
    Themes —主题管理中心,可以设置主题(支持鼠标选定,也支持写入配置文件生效),管理主题(删除及在线下载主题)<br>
    Updates — 目前功能只有一个,查询社区包的状态,随时随地的更新已安装的插件,Atom 软件的更新在 HELP 里面<br>
    Install — 目前分为两栏,自上而下,第一部分是搜索(可以搜索社区的插件),下面一部分会展示目前比较流行的插件(可以直接点击下载使用)<br>
    Open Config Folder — 这一块算不上鼠标操作控制,完全是软件的配置文件集合目录<br><br>
    
**前端插件推荐**<br>
参考：[Atom使用教程-插件主题推荐](https://wiki.jikexueyuan.com/project/atom/plug-in.html)&nbsp;&nbsp;[Atom的插件必备](https://www.jianshu.com/p/b779e2e5e3ef)&nbsp;不一 一列举<br><br>
1.emmet — 加快web开发速度，提供snippet(代码片段)、abbreviation expand(简写展开)功能。<br>
2.atom-beautify — 代码格式一键美化<br>
3.autoprefixer — 自动为 CSS 属性添加特定的前缀<br>
4.color-picker — 取色器,在编辑器里面挑选颜色<br>
5.linter — 代码校验工具(必备)<br>
&nbsp;&nbsp;  linter-jshint, for JavaScript and JSON, using jshint<br>
&nbsp;&nbsp;  linter-coffeelint, for CoffeeScript, using coffeelint<br>
&nbsp;&nbsp;  linter-tslint, for Typescript, using tslint<br>
&nbsp;&nbsp;  linter-php, for PHP using php -l<br>
&nbsp;&nbsp;  linter-pylint, for Python, using pylint<br>
&nbsp;&nbsp;  linter-scss-lint, for SASS/SCSS, using scss-lint<br>
&nbsp;&nbsp;  linter-less, for LESS, using less<br>
&nbsp;&nbsp;  linter-csslint, for CSS, using csslint<br>
&nbsp;&nbsp;  linter-stylint, for Stylus, using stylint<br>
&nbsp;&nbsp;  linter-stylus, for Stylus, using stylus<br>
6.autocomplete-xxx — 自动补全插件<br>
&nbsp;&nbsp;  autocomplete-paths — 路径补全，填写路径的时候有提示<br>
&nbsp;&nbsp;  autocomplete-html — html代码自动补全<br>
&nbsp;&nbsp;  autocomplete-css — css代码自动补全<br>
&nbsp;&nbsp;  autocomplete-snippets — 提示常用代码<br>
&nbsp;&nbsp;  autocomplete-python — python代码自动补全<br>
&nbsp;&nbsp;  autocomplete-bibtex — Github 的 markdown 语法<br>
7.less-autocompile — 实时编译，less文件编译为css文件<br>
&nbsp;&nbsp;  docblockr — 注释插件<br><br>

## 3.tips
Ctrl + Shift + P — 全局搜索面板<br>
Ctrl + Shift + M — .md文件预览<br><br>

**在Atom编辑器中如何全选带有连词符的单词：**<br>
在设置Settings里面,non word characters，删掉"-"<br>
![](https://segmentfault.com/img/bVRE63?w=804&h=443)<br>
![](https://segmentfault.com/img/bVRE7h?w=805&h=559)<br>
测试双击可选中<br>
![](https://segmentfault.com/img/bVRE7m?w=757&h=227)<br><br>
**Atom编辑器在哪里设置打开默认的浏览器**<br>
在设置Settings=>install里，搜索open-in-browser进行安装<br>
在Atom编辑器的html页面中，按快捷键Ctrl+Shift+P 调出全局搜索面板，按快捷键Ctrl+Shift+Q，或者输入o选择下图第3个，就可用默认浏览器打开html页面<br>
![](https://m.qpic.cn/psc?/V120flX00zHgB1/9XwfBMWIaa5Dh0kEemxh*FYDwJLYoxvQiXy*2D1rYjgBzKGk*c80qUnNEFzvxL5dNq1e9*WxnHwf.HSqZ7vIoQ!!/b&bo=qgKrAQAAAAADByA!&rf=viewer_4)<br>
markdown-preview-enhanced — Atom预览markdown插件：<br>
在atom中，先从file进入settings,选择install，搜索markdown-preview-enhanced，点击下载；<br>
选择packages，搜索markdown-preview，禁用它；<br>
在markdown-preview-enhanced下载完成后，enable（启用它）；<br>
导出pdf文件的方法：在atom中，先从file进入settings,选择install，搜索markdown-pdf，点击下载；<br><br>

## 4.快捷键    
<table><thead><tr><th align="center">英文</th>
  <th align="center">中文</th>
  <th align="left">快捷键</th>
  <th align="center">功能</th>
</tr></thead><tbody><tr><td align="center">New Window</td>
  <td align="center">新建界面窗口</td>
  <td align="left">Ctrl + Shift + N</td>
  <td align="center">如中文意思</td>
</tr><tr><td align="center">New File</td>
  <td align="center">新建文件</td>
  <td align="left">Ctrl + N</td>
  <td align="center">如中文意思</td>
</tr><tr><td align="center">Open File</td>
  <td align="center">打开文件</td>
  <td align="left">Ctrl + O</td>
  <td align="center">如中文意思</td>
</tr><tr><td align="center">Open Folder</td>
  <td align="center">打开文件夹</td>
  <td align="left">Ctrl + Shift + O</td>
  <td align="center">如中文意思</td>
</tr><tr><td align="center">Add Project Folder</td>
  <td align="center">加载项目目录</td>
  <td align="left">Ctrl + Alt + O</td>
  <td align="center">如中文意思</td>
</tr><tr><td align="center">Reopen Last Item</td>
  <td align="center">重新加载上次项目</td>
  <td align="left">Ctrl + Shift + T</td>
  <td align="center">如中文意思</td>
</tr><tr><td align="center">Save</td>
  <td align="center">保存文件</td>
  <td align="left">Ctrl + S</td>
  <td align="center">如中文意思</td>
</tr><tr><td align="center">Save As</td>
  <td align="center">另存为</td>
  <td align="left">Ctrl + Shift +S</td>
  <td align="center">如中文意思</td>
</tr><tr><td align="center">Close Tab</td>
  <td align="center">关闭当前编辑文档</td>
  <td align="left">Ctrl + W</td>
  <td align="center">如中文意思</td>
</tr><tr><td align="center">Close Window</td>
  <td align="center">关闭编辑器</td>
  <td align="left">Ctrl + Shift + W</td>
  <td align="center">如中文意思</td>
</tr><tr><td align="center">Undo</td>
  <td align="center">撤销</td>
  <td align="left">Ctrl + Z</td>
  <td align="center">如中文意思</td>
</tr><tr><td align="center">Redo</td>
  <td align="center">重做</td>
  <td align="left">Ctrl + Y</td>
  <td align="center">如中文意思</td>
</tr><tr><td align="center">Cut</td>
  <td align="center">剪切</td>
  <td align="left">Shift + Delete</td>
  <td align="center">如中文意思</td>
</tr><tr><td align="center">Copy</td>
  <td align="center">复制</td>
  <td align="left">Ctrl + Insert</td>
  <td align="center">如中文意思</td>
</tr><tr><td align="center">Copy Path</td>
  <td align="center">复制文档路径</td>
  <td align="left">Ctrl + Shift + C</td>
  <td align="center">如中文意思</td>
</tr><tr><td align="center">Paste</td>
  <td align="center">粘贴</td>
  <td align="left">Shift + Insert</td>
  <td align="center">如中文意思</td>
</tr><tr><td align="center">Select All</td>
  <td align="center">全选</td>
  <td align="left">Ctrl + A</td>
  <td align="center">如中文意思</td>
</tr><tr><td align="center">Select Encoding</td>
  <td align="center">选择编码</td>
  <td align="left">Ctrl + Shift +U</td>
  <td align="center">就是设置文件的编码</td>
</tr><tr><td align="center">Go to Line</td>
  <td align="center">跳转到某行</td>
  <td align="left">Ctrl + G</td>
  <td align="center">支持行列搜索,Row:Column</td>
</tr><tr><td align="center">Slect Grammar</td>
  <td align="center">语法选择</td>
  <td align="left">Ctrl + Shift + L</td>
  <td align="center">和Sublime的Syntax设置功能一样</td>
</tr><tr><td align="center">Reload</td>
  <td align="center">重载</td>
  <td align="left">Ctrl+ Alt +R</td>
  <td align="center">重新载入当前编辑的文档</td>
</tr><tr><td align="center">Toggle Full Screen</td>
  <td align="center">F11</td>
  <td align="left">全屏</td>
  <td align="center">如中文意思</td>
</tr><tr><td align="center">Increase Font Size</td>
  <td align="center">增大字体</td>
  <td align="left">Ctrl + Shift + “+”</td>
  <td align="center">Sublime的Ctrl + 也能生效</td>
</tr><tr><td align="center">Decrease Font Size</td>
  <td align="center">减小字体</td>
  <td align="left">Ctrl + Shift + “-“</td>
  <td align="center">Sublime的Ctrl - 也能生效</td>
</tr><tr><td align="center">Toggle Tree View</td>
  <td align="center">展示隐藏目录树</td>
  <td align="left">Ctrl + |Sublime的Ctrl+K,+B这里也可以生效</td>
  <td align="center"></td>
</tr><tr><td align="center">Toggle Commadn palette</td>
  <td align="center">全局搜索面板</td>
  <td align="left">Ctrl + Shift + P</td>
  <td align="center">和Sublime的大同小异</td>
</tr><tr><td align="center">Select Line</td>
  <td align="center">选定一行</td>
  <td align="left">Ctrl + L</td>
  <td align="center">如中文意思</td>
</tr><tr><td align="center">Select First Character of Line</td>
  <td align="center">选定光标至行首</td>
  <td align="left">Shift + Home</td>
  <td align="center">如中文意思</td>
</tr><tr><td align="center">Slect End of Line</td>
  <td align="center">选定光标至行尾</td>
  <td align="left">Shift + End</td>
  <td align="center">如中文意思</td>
</tr><tr><td align="center">Select to Top</td>
  <td align="center">选定光标处至文档首行</td>
  <td align="left">Ctrl + Shift + Home</td>
  <td align="center">就是光标处作为分割线,取文档上部分</td>
</tr><tr><td align="center">Select to Bottom</td>
  <td align="center">选定光标处至文档尾行</td>
  <td align="left">Ctrl + Shfit + End</td>
  <td align="center">就是光标处作为分割线,取文档下部分</td>
</tr><tr><td align="center">Find in Buffer</td>
  <td align="center">从缓存器搜索</td>
  <td align="left">Ctrl + F</td>
  <td align="center">与Sublime一致</td>
</tr><tr><td align="center">Replace in Buffer</td>
  <td align="center">高级替换</td>
  <td align="left">Ctrl + Shift + F</td>
  <td align="center">与Sublime一致</td>
</tr><tr><td align="center">Select Next</td>
  <td align="center">匹配选定下一个</td>
  <td align="left">Ctrl + D</td>
  <td align="center">和Sublime一模一样有木有</td>
</tr><tr><td align="center">Select All</td>
  <td align="center">匹配选定所有</td>
  <td align="left">Alt + F3</td>
  <td align="center">和Sublime一模一样有木有</td>
</tr><tr><td align="center">Find File</td>
  <td align="center">查询文件,选定打开</td>
  <td align="left">Ctrl + P</td>
  <td align="center">与Sublime不一样</td>
</tr><tr><td align="center">Delte End of Word</td>
  <td align="center">删除光标处至词尾</td>
  <td align="left">Ctrl + Del</td>
  <td align="center">如中文意思</td>
</tr><tr><td align="center">Duplicate Line</td>
  <td align="center">Ctrl + Shift + D</td>
  <td align="left">如中文意思</td>
  <td align="center"></td>
</tr><tr><td align="center">Delete Line</td>
  <td align="center">删除一行</td>
  <td align="left">Ctrl + Shift + K</td>
  <td align="center">如中文意思</td>
</tr><tr><td align="center">Toggle Comment</td>
  <td align="center">启用注释</td>
  <td align="left">Ctrl + /</td>
  <td align="center">与Sublime一致</td>
</tr><tr><td align="center">Toggle developer tools</td>
  <td align="center">打开Chrome调试器</td>
  <td align="left">Ctrl + Alt + I</td>
  <td align="center">神奇啊</td>
</tr><tr><td align="center">Indent</td>
  <td align="center">增加缩进</td>
  <td align="left">Ctrl + [</td>
  <td align="center">向右缩进</td>
</tr><tr><td align="center">Outdent</td>
  <td align="center">减少缩进</td>
  <td align="left">Ctrl + ]</td>
  <td align="center">向左缩进</td>
</tr><tr><td align="center">Move Line Up</td>
  <td align="center">行向上移动</td>
  <td align="left">Ctrl + up</td>
  <td align="center">如字面意思</td>
</tr><tr><td align="center">Move Line Down</td>
  <td align="center">行向下移动</td>
  <td align="left">Ctrl + Down</td>
  <td align="center">如字面意思</td>
</tr><tr><td align="center">Join Lines</td>
  <td align="center">行链接</td>
  <td align="left">Ctrl + J</td>
  <td align="center">追加</td>
</tr><tr><td align="center">newline-below</td>
  <td align="center">光标之下增加一行</td>
  <td align="left">Ctrl + Enter</td>
  <td align="center">与sublime 一致</td>
</tr><tr><td align="center">editor:newline-above</td>
  <td align="center">光标之上增加一行</td>
  <td align="left">Ctrl + Shift + Enter</td>
  <td align="center">与sublime 一致</td>
</tr><tr><td align="center">pane:show-next-item</td>
  <td align="center">切换编辑的标签页</td>
  <td align="left">Ctrl + Tab</td>
  <td align="center">如中文意思</td>
</tr><tr><td align="center">Fuzzy Finder</td>
  <td align="center">文件跳转面板</td>
  <td align="left">Ctrl + T</td>
  <td align="center">如字面意思</td>
</tr><tr><td align="center">Select Line Move above</td>
  <td align="center">选中行上移</td>
  <td align="left">Ctrl + up</td>
  <td align="center">如中文意思</td>
</tr><tr><td align="center">Select Line Move below</td>
  <td align="center">选中行下移</td>
  <td align="left">Ctrl + down</td>
  <td align="center">如中文意思</td>
</tr><tr><td align="center">Symbol-view</td>
  <td align="center">进入变量、函数跳转面板。</td>
  <td align="left">Ctrl + R</td>
  <td align="center">如中文意思</td>
</tr></tbody></table>
