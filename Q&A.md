#### 列举一些开源的云计算管理平台项目
OpenStack、Open vSwitch、Docker、Kubernetes
#### 云服务提供商提供的服务器安全组有什么用？

安全组是一种虚拟的防火墙。在安全组内可以放行系统相应的端口号以及IP访问的权限(如设置只能某些IP才可访问此台服务器)等。安全组具有数据包过滤、状态检测等功能，可以设置一系列的安全组规则来允许或禁止安全组内的ECS实例对公网或私网的访问，同时也可限制外部网络对ECS服务器的访问

参考：
[阿里云安全组](https://help.aliyun.com/document_detail/25387.html?source=5176.11533457&userCode=4phqzhon&type=copy)
& [浅谈云服务器安全组功能以及使用](https://www.cnblogs.com/xu-yi/p/10447013.html)

#### 为什么阿里云在国内的市场占有率要远远超过其他的几家厂商？
最早，最稳定，最成熟，投入最大
#### HTML 是一种编程语言吗？
`HTML`全称是超文本标记语言(Hyper Text Markup Language)，因此它跟`Python`, `C++`, `JAVA`等不一样，不是传统意义上的编程语言，而是一种标记语言(markup language)。由浏览器负责对`html`进行编译和渲染。

#### HTML、CSS、JavaScript 三者之间的关系是什么？
一个网页的正常运行一般需要三个要素HTML/CSS/JavaScript,分别代表框架，样式和行为。框架主要设定网页的不同地方放置不同的元素。而这个位置的内容以什么字体，什么颜色来显示就是样式。最后，这个位置的内容要传到后台的什么字段就是行为。

看过一个很有趣的比喻，假如整个网站是一个人的身体/那么HTML 是人的躯壳，CSS是人的五官和皮肤，JavaScript则是驱动整个人体活动的神经系统。
#### 简述 HTML、XHTML 和 XML的异同
#### 什么是 DOM?
DOM是文档对象模型(Document Object Model)的缩写，它是 HTML 文档的对象表示，同时也是 HTML 元素面向外部(如Javascript)的接口。

应用程序不是直接对`HTML`文档进行操作的，而是首先由浏览器对 html 文档进行分析。然后，应用程序通过浏览器所提供的 DOM 接口对分析结果进行操作，从而间接地实现了对 HTML 文档的访问。

DOM定义了HTML文档的**逻辑结构**，给出了一种访问和处理这两种文档的方法。
当服务器把html文件发送给浏览器的时候，浏览器会先读取出这个html文件的DOM树:


![dom tree](https://pic4.zhimg.com/80/a92533fd47b29c816efd3b4cf6cd614e_hd.jpg)

在[知乎](https://www.zhihu.com/question/34219998/answer/133487045)上看到一个比较有趣的比喻：
```
@破壁人王涛
    如果将文档的内容视为一栋办公楼，那DOM就是一种对办公楼内空间分配的标准，它规定了，这个办公楼的空间，应该是先分楼层，再分房间的方式，方便访客找到这个房间。有什么用？

    举例说明：你要去一个叫201的房间（获取对象），你怎么去呢? 用DOM的方法，你只需要走到二层，然后到第一个房间就行了，而你是用走，爬，甚至跳舞的方式过去（即：使用不同的编程语言）都没关系，你只要按照DOM的规定，最终都能找到这个房间。

    全世界的房子都是分楼层，再分房间的结构，于是，你去哪个办公楼找人，你都能通过上某个楼层、按照房间的排列顺序去找到某个房间。

    同理全世界的网页内容都是DOM的结构，于是，你去找网页中的某个对象时，都能通过某个标签的某个子标签找到某个对象。

```
#### 现在的网页 HTML 文件一般会包含哪些 HTML 标签？
`<html></html>`
`<head></head>`
`<meta></meta>`

`<body></body>`
`<table></table>`
`<tr></tr>`
`<td></td>`
`<li></li>`
`<a></a>`
`<link>`(开放标签)
`<script></script>`
`<style></style>`

...

[参考手册](https://www.runoob.com/tags/html-reference.html)

#### CSS 选择器有哪些？
CSS选择器用于选择你想要的元素的样式的模式。HTML页面中的元素就是通过CSS选择器进行控制的。

每一条css样式定义由两部分组成，`选择器{样式}`。 “选择器”指明了`{}`中的“样式”的作用对象，也就是“样式”作用于网页中的哪些元素。CSS选择器大致分为：

 - 类选择器: `.class`
 - id选择器: `#id`
 - 标签选择器
 - 元素选择器
 - 后代选择器
 - 子元素选择器

更多参考：[CSS选择器参考手册](http://www.w3school.com.cn/cssref/css_selectors.asp)
#### Chrome，Safri，Firefox 如何查看网页源代码并快速定位元素？快捷键是什么？
大部分浏览器按`F12`就可以调出开发页面， `Ctrl+U`可以打开页面源代码
#### 有哪些常用的 Chrome 插件可以用于网页服务开发调试？
`postman`:可以调试简单的css、html、脚本等简单的网页基本信息，还可以发送几乎所有类型的HTTP请求。
官方文档 [postman](https://www.getpostman.com/docs/v6/)

`Chrome Dev Tools`:Chrome本身的Chrome DevTools就是一个很好的开发调试工具。更多使用方法可以看：[你不知道的Chrome DevTools](https://segmentfault.com/a/1190000000494090)
#### 目前常见的前端框架有哪些？分别罗列一些使用这些框架的生物信息学数据库/网页服务
#### HTML 元素和 Markdown 之间的对应关系
语法种类很少，只对应 HTML 标记的一小部分
块级HTML元素内是不能使用Markdown语法
#### document.getElementById 是用来做什么的？
HTML DOM 定义了多种查找元素的方法,当你需要查找文档中的一个特定的元素，`getElementById()` 可返回对拥有指定 ID 的第一个对象的引用。所以在操作文档的一个特定的元素时，最好给该元素一个 id 属性，为它指定一个（在文档中）**唯一**的名称，然后就可以用该 ID 查找想要的元素。

参考：[HTML DOM getElementById() 方法](http://www.w3school.com.cn/jsref/met_doc_getelementbyid.asp)
#### JavaScript 的运行速度和 Python/R 相比是快还是慢？
javacript > pyhon > R

（可以用斐波那契数列验证）
#### Cookie 和 Session 存在的目的是什么？

一般而言是为了让用户保持登录状态。
 客户端（用户）第一次访问一个服务器时，服务器会生成一个**Cookie**和**Session**。前者保存在客户端浏览器中，后者保存在服务器中，session比cookie更安全。下一次这个客户端再访问这个服务器时，服务端通过携带的Cookie找出该用户信息。服务端就能够知道是谁访问了。(p.s. `Session` 是对服务端来说的, 客户端没有 Session 这一说)。
 ![](https://ask.qcloudimg.com/http-save/developer-news/146u28ouxj.jpeg?imageView2/2/w/1620)

 另外，对于 API 还有一个token的概念，详细可见：

 [Cookie，Session和Token概念的正确理解](https://cloud.tencent.com/developer/news/247610)

#### JavaScript 数据有哪些类型？它和 R/Python 的数据类型是否有什么对应关系？

    JavaScript的数据类型分为两大类，基本数据类型和复杂数据类型。

 - 基本数据类型：Null、Undefined、Number，String，Boolean。
 - 复杂数据类型：Object。

#### 如何设置多个 git 远程仓库，并分别推送和拉取？
#### GitHub 克隆仓库时选择 git:// 和 https://的差异
#### 什么是持续集成？
#### 什么是敏捷开发？
#### GitHub 仓库可以关联哪些第三方网页服务进行发布前的自动测试？
#### GitHub 的 Webhook 可以用来做什么？
#### MySQL 的开源版本叫什么？它和甲骨文公司维护的版本有什么区别？
#### MySQL 和 SQLite 分别适用于哪些网页应用程序？
#### SQLite 数据库能否设置用户名和密码？
#### 在 R/Python 中提供SQLite 和 MySQL 接口的包/模块分别是？

#### 使用最基础的 HTML/CSS/JavaScript 语法，设计一个简单的单页网页界面（至少应该包含一二三级标题和正文、表格、内容分栏、超链接、图片、视频、点击动画等）
#### 使用 JavaScript 编写一个可以生成斐波那锲数列的函数，输入为n，表示该数列所包含的数字个数

    斐波那契数列(Fibonacci)也叫兔子数列。
    在第一个月有一对刚出生的小兔子，在第二个月小兔子变成大兔子并开始怀孕，
    第三个月大兔子会生下一对小兔子，并且以后每个月都会生下一对小兔子。
    如果每对兔子都经历这样的出生、成熟、生育的过程，并且兔子永远不死，
    那么兔子的总数是如何变化的？
  ![兔子问题](https://ss2.baidu.com/6ONYsjip0QIZ8tyhnq/it/u=3476100182,2210271329&fm=173&app=25&f=JPEG?w=457&h=412&s=8532EC33150AD4EC0258B9D20200F0B1)

其实是一个**数列问题**，根据列出下表：
![](https://ss0.baidu.com/6ONWsjip0QIZ8tyhnq/it/u=3499102896,3228291657&fm=173&app=25&f=JPEG?w=640&h=135&s=8D2E7433C523693002D585CA000070B3)
我们可以得到两个信息：
 1. 从3个月（n=3)开始，小兔子的数量跟前一个月(n=2)大兔子的数量是一致的。
 2. 从3个月（n=3)开始，大兔子的数量是前一个月(n=2)大兔子和小兔子的总和。


    按照这个表格，我们会发现无论是小兔子对数、大兔子对数还是总对数，
    除了最初几个数字不一样之外，
    后面都是按照1、1、2、3、5、8、13…变化的。
    个数列就称为兔子数列或者斐波那契数列。
    兔子数列最大的特点就是前两项之和等于后一项
用an表示一个数列的第n项，那么斐波那契数列的规律就是:

  **a<sub>1</sub>=1**

  **a<sub>2</sub>=1**

  **a<sub>n+2</sub> = a<sub>n</sub>+a<sub>n+1</sub>**

或者是

n=0,    f(n)=0

n=1,  f(n)=1   

n>=1, f(n)=f(n-1)+f(n-2)

  这是一种递归函数。
用Javascript实现斐波那契数列：
```JavaScript
function Fibonacci(n) {
  if (n==0){return 0}
  if (n==1){return 1}
  if (n>=1){
    return Fibonacci(n-1)+Fibonacci(n-2) }
}
```
参考：[什么是斐波那契数列](https://baijiahao.baidu.com/s?id=1606651492697783298&wfr=spider&for=pc)

#### 比较相同功能的函数在JavaScript，R，和 Python 之间的差别（语法+速度）
#### 尝试本地部署 Gitlab 服务
Gitlab 是一个代码仓库管理系统，可以很方便的管理权限、代码review，创建、管理project。你可以用gitlab自己搭建一个类似于Github一样的系统，一般用于在企业、学校等内部网络搭建git私服。

参考资料：

[在本地服务器搭建gitlab仓库管理](https://www.cnblogs.com/nulige/p/6825625.html)

[手把手教你 GitLab 的安装及使用](https://www.jianshu.com/p/b04356e014fa)
