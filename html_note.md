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
