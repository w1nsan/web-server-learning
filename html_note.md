**HTML元素**指的是从开始标签到结束标签的所有代码。

<开始标签>HTML元素<结束标签>

### HTML语法
 - 使用小写标签
 - HTML 元素以开始标签起始
 - HTML 元素以结束标签终止
 - 元素的内容是开始标签与结束标签之间的内容
 - 某些 HTML 元素具有空内容（`empty content`）
 - 空元素在开始标签中进行关闭（以开始标签的结束而结束）比如说`<br/>`
 - 大多数 HTML 元素可拥有属性

### 嵌套的HTML
大部分的HTML元素是可以嵌套的（即，可以包含其他HTML元素）

### 元素实例

##### `<div></div>`
 一个盒子，用于容纳其他的元素,用来分类和嵌套样式

##### `<a></a>`
添加链接 （锚链接）

<a href="http://bilibili.com" target="_blank">我是一个链接</a>

`target="_blank"`代表另起一个新窗口

'href' 属性
'target'属性

##### <img>标签
插入图片
只有开始，没有结束。不能含有子元素，不能嵌套
<img src="">网络
<img src="本地地址.gif" alt="当你看见我就代表图片挂了"> 本地

#### 表格相关的标签
`<table>` 建立一个表格
<tr> 代表一行
<td> 代表单元格的内容
<th> 代表head 每一列的表头
<thead> 盒子，把表头<th>的内容包进去
<tbody> 盒子，把剩下的数据包进去


---
##### <header> 盒子，标题内容
<header>
	<h1></h1>
    <small>副标题
</header>
##### <footer> 盒子，指定页脚
<footer>（term/privacy/contact/about us)
</footer>
<hr> 水平线

###### 关于这些`盒子`
三者都是干净的“盒子”，header和footer跟div的区别是，它们是有语义的，在搜索引擎搜索时可以马上区分优先顺序。


##### <link>
没有结束标签；给页面指定样式表,加载样式表,一般放在<head>里
<head>
  <link href="指定某张css表的地址">
</head>

##### <script></script>
加载JavaScript脚本，一般放在`<body>`里。js可以放在最后（依赖不强时）
<body>
  <script src="base.js"></script>
</body>

##### <button></button> 按键标签
单独存在时意义不大。要跟JS连接；或者提交表单：
```HTML
<form>
user:<input><br/>
psw:<input><br/>
<button>conform</button>
</form>
```
<br/>敲断行

##### <abbr></abbr> 添加缩写
例子：
```HTML
<abbr title="hyper text...">HTML</abbr>
```
语义确定的标签。
跟<span>相似。

---
<code></code>行内元素，放置代码  等宽字体

<pre></pre>放大段代码。前后另起一行，等宽字体

### HTML 属性

 - HTML 标签可以拥有属性。属性提供了有关 HTML 元素的更多的信息。

 - 属性总是以`名称=值`的形式出现，比如：name="value"。

 - 属性总是在 HTML 元素的**开始标签**中规定。
 - 始终为属性加引号

 - 属性要用小写

 -大多数HTML元素的属性：`class`, `id`, `style`, `title`

### 注释
```HTML
<!-- 注释 -->
```
合理地使用注释可以对未来的代码编辑工作产生帮助。
注释标签**不支持**任何事件属性。

### DOCTYPE
 - <!DOCTYPE> 声明必须是 HTML 文档的第一行，位于 <html> 标签之前。

 - <!DOCTYPE> 声明不是 HTML 标签；它是指示 web 浏览器关于页面使用哪个 HTML 版本进行编写的指令。

 - HTML5中只有一种声明：
`<!DOCTYPE html>`

 - <!DOCTYPE> 声明对大小写**不敏感**。

HTML 的标准属性和事件属性指的分别是什么？

## 头部
### `head` 里的相关标签
`head` 元素包含了所有的头部标签元素。在 `head`元素中你可以插入脚本（scripts）, 样式文件（CSS），及各种`meta`信息。

```
可以添加在头部区域的元素标签为: <title>, <style>, <meta>, <link>, <script>, <noscript>, and <base>.
```
主要内容
  * title 元素
  * base 元素
  * link 元素
  * meta 元素

#### base 标签
 `<base>` 标签可以在开头用来定义**全局**的链接。包括设置链接的绝对路径(`href`)，打开方式(`target`)（原有窗口还是新窗口）这样后面`body`中的各种链接就自动赋予了相应的属性，不需要一个个地去设置。
 ```html
 <!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<title>菜鸟教程(runoob.com)</title>
<base href="//www.runoob.com/images/" target="_blank">
</head>

<body>
<img src="logo.png"> - 注意这里我们设置了图片的相对地址。能正常显示是因为我们在 head 部分设置了 base 标签，该标签指定了页面上所有链接的默认 URL，所以该图片的访问地址为 "http://www.runoob.com/images/logo.png"
<br><br>
<a href="//www.runoob.com">菜鸟教程</a> - 注意这个链接会在新窗口打开，即便它没有 target="_blank" 属性。因为在 base 标签里我们已经设置了 target 属性的值为 "_blank"。

</body>
</html>
```

---

#### `link` 标签

`link`元素用来链接到**外部样式文件**（一般是CSS样式）
```html
<head>
<link rel="stylesheet" type="text/css" href="theme.css">
</head>
```
##### 注意：

`<link>标签`只能在`<head>`中。不过它可出现任何次数。

`<link>标签`是空元素：只有**属性**，没有内容，也没有结束标签。

`rel`是**必须属性**。定义当前文档与被链接文档之间的关系。

[link属性](https://www.runoob.com/tags/tag-link.html)

---
