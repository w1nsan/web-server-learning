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
`<tr>` 代表一行
`<td>` 代表单元格的内容(table data)
`<th>` 代表head 每一列的表头
`<thead>` 盒子，把表头<th>的内容包进去
`<tbody>` 盒子，把剩下的数据包进去

```HTML
<!--不带边框的表格-->
<table class="table">
 <caption>inhibition of par modification</caption>
 <!--设置表格的标题-->
 <thead>
 <!--水平表头-->
  <th>siNC</th>
  <th>siPARP1</th>
  <th>mock</th>
  <th>olaparib</th>
 </thead>
 <tbody>
 <tr>
  <td>0.1</td>
  <td>0.2></td>
  <td>0.4</td>
  <td>0.2</td>
 </tr>
 </tbody>
</table>

 <table boder="1" cellpadding="10">
 <!--设置了单元格边距-->
 <!--垂直表头-->
 <tr>
  <th>siNC</th>
  <td>0.1</td>
 </tr>
 <tr>
  <th>siPARP1</th>
  <td>0.2</td>
 </tr>
 <tr>
  <th>mock</th>
  <td>0.4</td>
 </tr>
 <tr>
  <th>olaparib</th>
  <td>0.2</td>
 </tr>
 </table>
```

---
##### `<header>` 盒子，标题内容
```HTML
<header>
	<h1></h1>
    <small>副标题
</header>
```
##### `<footer>` 盒子，指定页脚
```HTML
<footer>（term/privacy/contact/about us)
</footer>
<hr> 水平线
```
###### 关于这些`盒子`
三者都是干净的“盒子”，header和footer跟div的区别是，它们是有语义的，在搜索引擎搜索时可以马上区分优先顺序。

---

##### `<link>`标签
没有结束标签；给页面指定样式表,加载样式表,一般放在`<head>`里：
```HTML
<head>
  <link href="指定某张css表的地址">
</head>
```
##### `<script></script>`标签
加载** JavaScript 脚本**，一般放在`<body>`里。js可以放在最后（依赖不强时）

<body>
  <script src="base.js"></script>
</body>

##### `<button></button>` 按键标签
单独存在时意义不大。要跟JS连接；或者提交表单：
```HTML
<form>
user:<input><br/>
psw:<input><br/>
<button>conform</button>
</form>
```
`<br/>`敲断行

##### `<abbr></abbr>` 添加缩写
例子：
```HTML
<abbr title="hyper text...">HTML</abbr>
```
语义确定的标签。
跟`<span>`相似。

---
`<code></code>`行内元素，放置代码  等宽字体

`<pre></pre>`放大段代码。前后另起一行，等宽字体

### HTML 属性

 - HTML 标签可以拥有属性。属性提供了有关 HTML 元素的更多的信息。

 - 属性总是以`名称=值`的形式出现，比如：`name="value"`。

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

### `DOCTYPE`
 - <!DOCTYPE> 声明必须是 HTML 文档的第一行，位于 <html> 标签之前。

 - <!DOCTYPE> 声明不是 HTML 标签；它是指示 web 浏览器关于页面使用哪个 HTML 版本进行编写的指令。

 - HTML5中只有一种声明：
`<!DOCTYPE html>`

 - <!DOCTYPE> 声明对大小写**不敏感**。

`HTML` 的标准属性和事件属性指的分别是什么？

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
 `<base>` 标签可以在开头用来定义**全局的链接**。包括设置链接的绝对路径(`href`)，打开方式(`target`)（原有窗口还是新窗口）这样后面`body`中的各种链接就自动赋予了相应的属性，不需要一个个地去设置。
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
#### `style`标签
（style 既是标签，也是属性）

`<style>` 标签定义了HTML文档的样式文件引用地址.
在`<style>` 元素中你也可以**直接添加**样式来渲染 HTML 文档
```HTML
<head>
<style type="text/css">
body {background-color:yellow} #直接添加样式，定义了body
h1 {color: pink;}
p {color:blue;}  #直接添加样式，定义了段落 p
</style>
</head>
```

`style`和`link`跟样式表都有关系，但是:
> 如需链接外部样式表，请使用 **link** 标签。

##### `style`标签的`scoped`属性

`scoped` 属性是 `HTML 5 `中的新属性，它允许我们为文档的指定**部分**定义样式，而不是整个文档。

如果使用 `scoped` 属性，那么所规定的样式只能应用到 `style` 元素的父元素及其子元素。
***目前只有 Firefox属性支持 scoped 属性***  ┑(￣Д ￣)┍

#### `meta` 标签

`meta`标签描述了一些基本的元数据。这些元数据也不显示在页面上，但会被浏览器解析。

`meta`元素通常用于指定网页的描述，关键词，文件的最后修改时间，作者，和其他元数据。可以使用于**浏览器**（如何显示内容或重新加载页面），**搜索引擎**（关键词），或其他Web服务。

`<meta>`一般放置于 `<head>` 区域
常用属性有：`name` ,`http-equiv` ,`charset`三种。


一般的定义格式：
```html
<meta name="元数据名称" content="元数据的值/内容">
```
eg.1 为搜索引擎定义**关键词**：
```html
<meta name="keywords" content="HTML,CSS,XML,XHTML,JAVASCRIPT">
```
eg.2 为网页定义描述内容（读者看不见但浏览器会解析）：
```html
<meta name="description" content="code, web, website">
```
eg.3 定义网页作者（读者也是看不见的）：
```html
<meta name="author" content="runoob">
```
eg.4 还可以定义网页的**显示方式**，比如说每隔30s，刷新页面：
```html
<meta http-equiv="refresh" content="30">
```
##### 另外
在`HTML5` 中，有一个新的 `charset` 属性，它使字符集的定义更加容易：
```html
 <meta charset="UTF-8">
 <!--定义文档的字符编码-->
 ```


### `<script>`标签
用于加载脚本文件，比如： `JAVASCRIPT`（在html中，基本都只有js的脚本了。）

### `HTML`列表
#### 无序列表 `<ul>`标签
`<li>`是列表项
```HTML
<ul>
  <li>coffee</li>
  <li>milk</li>
  <li>tea</li>
 </ul>
```
#### 有序列表 `<ol>`标签
```HTML
<ol>
  <li>coffee</li>
  <li>milk</li>
  <li>tea</li>
</ol>
```
##### 不同类型的有序标签
通过设定`type` 属性
```HTML
<ol type="i">
<li>coffee
  <ul>
    <li>latte</li>
    <li>flat white</li>
   </ul>
</li>
<li>milk</li>
<li>tea</li>
</ol>
```
显示如下：
<ol type="i">
<li>coffee
  <ul>
    <li>latte</li>
    <li>flat white</li>
   </ul>
</li>
<li>milk</li>
<li>tea</li>
</ol>

```HTML
<ol type="A">
<li>coffee</li>
<li>milk</li>
<li>tea</li>
</ol>
```
效果如下：
<ol type="A">
<li>coffee</li>
<li>milk</li>
<li>tea</li>
</ol>
