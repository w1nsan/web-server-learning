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
### 外部引用
当样式需要被应用到**很多页面**的时候，外部样式表将是理想的选择。使用外部样式表，你就可以通过更改一个文件来改变整个站点的外观。

**使用`<link>`元素**

```HTML
<head>
<link rel="stylesheet" type="text/css" href="mystyle.css">
<!--这里的 href 属性使用的是相对路径-->
</head>
```
---
## CSS的语法
### 书写规则
CSS 规则由两个主要的部分构成：
 - 选择器 （你想改变的对象）
 - 一条或多条声明 （你想对该对象的什么外观进行定义）

CSS声明总是以分号(;)结束，声明组以大括号({})括起来
 ```css
 选择器 {属性：值；属性：值；}

 ```

 ![css语法](https://www.runoob.com/wp-content/uploads/2013/07/632877C9-2462-41D6-BD0E-F7317E4C42AC.jpg)

##### 案例 对`p`进行声明
```css
p {color:red;text-align:center;}
```
为了让声明**更具有可读性**,可以分段：
```css
p
{
  color:red;
  text-align: center;

}
```
##### CSS 的注释
CSS的注释和 html 的不一样,语法是：`/*注释内容*/`。
```css
/*这是个注释*/
p
{
text-align:center;
/*这是另一个注释*/
color:black;
font-family:arial;
}
```
### 如何在 HTML 元素中添加 CSS 样式
——使用 **`id`**和 **`class`选择器**。

如果你要在HTML元素中设置CSS样式，你需要在**元素中**设置`id` 和 `class` 选择器。

#### id 选择器 (一般针对一个/特定元素)
id 选择器可以为**标有特定 id **的 HTML 元素指定特定的样式

如果你在某个元素的属性里添加了`id`
```HTML
<p id="para1">我是段落</p>
<!--ID属性不要以数字开头，数字开头的ID在 Mozilla/Firefox 浏览器中不起作用。-->
```
当你想用 CSS 来定义这个`<p>`的样式时，就可以使用你设置的`id`来选择它。
```css
/*在 css 中用 "#"来选择 id */
#para1
{
    text-align:center;
    color:red;
}
/*这个 css 对 html中的 p 进行样式的定义*/
```
#### class 选择器 （可同时定义多个元素）
class 选择器用于描述**一组元素**的样式，`class`选择器有别于`id`选择器，`class`可以在**多个元素**中使用。

下面设置一组 html 元素：
```html
<h1 class="import"></h1>
<p class="import"></p>
<p class="not_import"></p>
```
    关于class的定义：
     - classname不能以数字开头，区分大小写。
     - 如需为一个元素规定多个类，用空格分隔类名



在 CSS 中，类选择器以一个点**`.`**号显示：
```css
.import {text-align:center;}
/* 对于 class 为 import 的元素，文字都显示居中 */
```
也可以在某种特定的元素中指定 class
```css
p.import {text-align:center;}
/* <p>元素中，类别为 import的文字都居中，但是这时候<h1>的样式不会被改变；
```
