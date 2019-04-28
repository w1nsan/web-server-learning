# CSS
CSS (Cascading Style Sheets) 用于渲染 HTML 元素标签的样式。

### 如何使用 CSS
CSS 可以通过以下方式添加到 HTML 中:

 - **内联样式**- 在HTML元素中使用`style` **属性**
 - **内部样式表** -在HTML文档头部 `<head>` 区域使用`<style>`**元素** 来包含CSS
 - **外部引用** 使用外部 CSS 文件,使用`<link>`

#### 内联样式
对单个元素逐一设置 `style`属性，这种设定一般只针对单个元素，就好比只设置人体中某一块皮肤的颜色一样。
##### 例 1 添加一个没有下划线的链接
```HTML
<!DOCTYPE html>
<html>

<head>
  <meta charset="utf-8">
  <title>css的使用</title>
</head>

<body>
  <a href="//www.baidu.com/" style="text-decoration:none;">测试一下你的网速吧(●ˇ∀ˇ●)</a>
  <!--这里的style只对这个链接设置了没有下划线，但其他地方的链接还是会有的，这是一种局部设置-->
</body>

</html>
```
### 内部样式表
当**单个文件**需要特别样式时，就可以使用内部样式表。你可以在`<head>` 部分通过**`<style>`标签**定义内部样式表。（so, `Style` 既是属性也是标签啊！）
```html
<!DOCTYPE HTML>
<head>
  <meta charset="utf-8">
  <title>CSS从开门到入门</title>
  <style type="text/css">
  body
  {
    background-color: yellow;
  }
  p
  {
    color: blue;
    font-family:"Times New Roman";
  }
  </style>
  <!--在 style 这个“盒子”里，装进你想这个文件所产生的样式效果-->
</head>
<body>

```
