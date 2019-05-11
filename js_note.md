#### Node.js

##### 定义
`Node`是一个服务器端 `JavaScript 解释器``，它将改变服务器应该如何工作的概念。它的目标是帮助程序员构建高度可伸缩的应用程序，编写能够处理数万条同时连接到一个（只有一个）物理机的连接代码。

    `Node.js` 是一个让 `JavaScript` 运行在浏览器之外的平台。

它实现了诸如文件系统、模块、包、操作系统 `API`、网络通信等 `Core JavaScript` 没有或者不完善的功能。

历史上将 `JavaScript`移植到浏览器外的计划不止一个，但`Node.js` 是最出色的一个。

##### CommonJS 规范
随着`Node.js` 的成功，各种浏览器外的 `JavaScript` 实现逐步兴起，因此产生了 **`CommonJS 规范`**。

`CommonJS` 试图拟定一套完整的 `JavaScript` 规范，以弥补普通应用程序所需的 `API`，譬如文件系统访问、命令行、模块管理、函数库集成等功能。

`CommonJS` 制定者希望众多服务端 `JavaScript` 实现遵循 `CommonJS` 规范，以便相互兼容和代码复用。

`Node.js` 的部份实现遵循了`CommonJS`规范，但由于两者还都处于诞生之初的快速变化期，也会有不一致的地方。

---
---
# JavaScript 基础
###### 廖雪峰教程笔记

## 基本概念
 - JavaScript 除了语法上有点像 Java，其他部分基本上没啥关系

 - 几个公司联合 `ECMA`（European Computer Manufacturers Association）组织定制了 JavaScript 语言的标准，被称为 `ECMAScript` 标准。如果你遇到 `ECMAScript`这个词，简单把它替换为 `JavaScript` 就行了。

 - 讲到`JavaScript` 的**版本**，实际上就是说它实现了`ECMAScript`标准的哪个版本。（最新版`ECMAScript 6`标准，简称`ES6`）。

## 入门内容
### 添加 js 到 html 中
JavaScript 代码可以直接嵌在网页的任何地方，不过通常我们都把 JavaScript 代码放到 `<head>` 中。（也有说放到`<body>`的结尾处，防止js出错了，整个html的解析都出问题）

 ```HTML
<html>
  <head>
  /* 将js代码或文件放到 script 中 */
    <script>
      alert<"what's up, man";>
    </script>
  </head>
  <body>
    <p></p>
  </body>
</html>
 ```
如果是通过添加一个 `js`文件，可用 `src`属性：
```HTML
<script src="a/b/file.js"></script>
```
把 JavaScript 代码放入一个单独的`.js`文件中更**利于维护代码**，并且多个页面可以各自引用同一份`.js`文件。

### js语句书写
JavaScript的语法中每个语句以`;`结束，语句块用花括号`{...}`

最好不要**一行**写多个语句。

#### 语句块
**语句块**是一组语句的集合，例如，下面的代码先做了一个**判断**。如果判断成立，将执行 `{...}` 中的所有语句：

```js
// 在 md 中，JavaScript的代码块引用是 js
  if (2 > 1){
    x = 1;
    y = 2;
    z = 3;
  }
// 缩进不是JavaScript语法要求必须的，但缩进有助于我们理解代码的层次
// 所以编写代码时要遵守缩进规则。
```
还可以写成**层级结构**，也就是花括号里套花括号：
```js
  if (2 > 1){
    x = 1;
    y = 2;
    if (x < y){
      z = 3
      q = 4
      if (z < q){
        z = 5
      }      // 最里层语句块
    }
  } //最外层语句块
```
JavaScript 本身对嵌套的层级没有限制，但是过多的嵌套无疑会大大增加看懂代码的难度。

遇到这种情况，需要把部分代码抽出来，作为**函数(function)**来调用，这样可以减少代码的复杂度。

#### 注释

行注释：
```js
// 我是行注释，从斜杠开始到行结束都是注释;
```
注释块：
```js
/* 注释块开始;
阔以写很多行;
连续的很多行;
记得关闭起来; */
```
#### 语句大小写
**注意！**

`JavaScript` 严格**区分**大小写，如果弄错了大小写，程序将报错或者运行不正常。

### 数据类型和变量

  计算机能处理的远不止数值，还可以处理文本、图形、音频、视频、网页等各种各样的数据，不同的数据，需要定义不同的**数据类型**。

#### 数字
`NaN`是一个特殊的 number。代表缺失值。
#### 字符串

#### 布尔值

##### 与运算 (&&)
所有值为`true`,结果才是 `true`。
##### 或运算 (||)
其中一个值为 `true`,结果就是 `true`。
##### 非运算 (!)
`!运算`是非运算，它是一个单目运算符，把`true`变成`false`，`false`变成`true`：
```js
!false;//结果为 true
!true; //结果为 false
!(2 > 5); //结果为 true
```

布尔值经常用在条件判断中
```js
var age = 15
if (age > 18;){
  alert ("well,then you are an adult";)//布尔值为true
} else{
  alert ("kid,close the window!") //布尔值为false
}
```
##### 比较运算
可以通过比较运算符 `>`,`<`,`==`,`===`等来对数字或者其他类型数据进行比较从而得到**布尔值**。
###### 关于相等运算符
第一种是`==`比较，<span style="border-bottom:2px dashed pink;">它会自动转换数据类型再比较</span>，很多时候，会得到非常诡异的结果；

第二种是`===`比较，<span style="border-bottom:2px dashed pink;">它不会自动转换数据类型</span>，如果数据类型不一致，返回`false`，如果一致，再比较。

由于`JavaScript`这个设计缺陷，不要使用`==`比较，**始终坚持使用`===`比较。**

此外，`NaN`这个特殊的 Number 与所有其他值都**不相等**，包括它自己：
```js
NaN === NaN; //结果是 false
```
唯一能判断`NaN`的方法是通过`isNaN()`函数：
```js
isNaN(NaN); //结果是 true
```

###### 浮点数比较
浮点数在运算过程中会产生**误差**，因为计算机无法精确表示无限循环小数。要比较两个浮点数是否相等，只能计算它们之差的**绝对值**，看是否小于某个**阈值**：
```js
1 / 3 === (1 - 2 / 3); // false
// 比较两个浮点数的差值是否小于某个阈值
Math.abs(1 / 3 - (1 - 2 / 3)) < 0.0000001; // true
// Math.abs() 返回绝对值
```
#### null & undefined
`null`表示一个“空”的值，它和`0`以及空字符串`''`不同，`0`是一个数值，`''`表示长度为`0`的字符串，而`null`表示“空”。

JavaScript的设计者希望用`null` 表示一个空的值，而`undefined`表示值未定义。事实证明，这并没有什么卵用，区分两者的意义不大。**大多数情况下，我们都应该用`null`**。`undefined`仅仅在判断函数参数是否传递的情况下有用。
#### 数组
数组是一组按顺序排列的集合，集合的每个值称为元素。JavaScript的数组可以包括任意数据类型。例如：
```js
[1,2,3,a,b,c,null,true]; //虽然说是“数”组，但是任何数据类型都可以作为“元素”放进来
```
数组用`[]`表示，元素之间用`,`分隔。
##### 用函数创建数组
```js
new Array(1, 2, 3); // 创建了数组[1, 2, 3]
```
##### 建议用法
然而，出于代码的可读性考虑，强烈建议直接使用`[]``。

数组的元素可以通过**索引**来访问。请注意，索引的起始值为`0`：
```js
var my_arr = [1, 2, 3.14, 'Hello', null, true];
my_arr[0]; // 返回索引为0的元素，即1
my_arr[5]; // 返回索引为5的元素，即true
my_arr[6]; // 索引超出了范围，返回undefined
```

[几个创建数组方法之间的区别](https://www.jianshu.com/p/75a45851b655)
#### 对象
JavaScript的对象是一组由键-值组成的无序集合.
比如说有一个对象(person)，设置6个键（**=属性**）：name,age,sex,tags,city,hasCar;每个键（属性）里面包含了对应的值(任意数据类型)。

`对象{属性：值；}`
```js
var person = {
  name:"winsan", //属性名是字符串 name，属性的值是 “winsan”
  age:20,
  sex:"female",
  tags:[geek,lab,crazy,kind],
  city:"guangzhou",
  hasCar:false
}
```
如果想获取某个对象的某个属性值，需要用 `对象.属性名`的方式：
```js
person.name; //返回名字属性的值，比如说 “winsan”
person.hasCar;//false
```

#### 变量

##### 变量赋值
在js中，用等号 `=`给变量赋值（**注意不要和判断符号的等号弄混了**）
申明一个变量用`var`语句:
```js
var a; //申明变量 a，但a没有值，是 undefined
var $b = 1; //申明变量 $b,同时赋值
var s_010 ="010";//s_010的值是一个字符串 "s_010"
var answer = true;//赋予布尔值
var t =null; //t的值是空的 Null
```
尽量不要用中文作为变量名。
##### 动态语言
在`JavaScript`中，使用等号`=`对变量进行赋值。可以把任意数据类型赋值给变量，同一个变量可以反复赋值，而且可以是不同类型的变量，<span style="border-bottom:2px dashed green;">但是要注意只能用var申明一次</span>，例如：
```js
var a = 20; //申明一个变量a，并赋值20
a = "abc";//对a重新赋值成一个字符串，但此时不需要再申明了
```
这种不需要事先给变量指定特定类型的就叫 **动态语言**
##### 变量内容的查看
要显示变量的内容，可以用
```js
console.log(x)
```
使用`console.log()`代替`alert()`的好处是可以避免弹出烦人的对话框。

##### 为什么要申明变量
如果一个变量没有通过`var`申明就被使用，那么该变量就自动被申明为**全局变量**。在同一个页面的不同的 JavaScript 文件中，如果都不用`var`申明，恰好都使用了变量`i`，将造成变量`i`互相影响，产生难以调试的错误结果。

因此一般情况下我们要使用 `strict`功能，强制对每个变量事先申明，否则浏览器报错。

```js
'use strict'; //开启strict
```
这是一个字符串，不支持`strict模式`的浏览器会把它当做一个字符串语句执行，支持`strict模式`的浏览器将开启`strict模式`运行 JavaScript。

### 数据类型——字符串

#### 转义字符
转义字符`\`可以转义很多字符，比如`\n`表示换行，`\t`表示制表符，字符`\`本身也要转义，所以`\\`表示的字符就是`\`。

`ASCII字符`可以以`\x##`形式的十六进制表示，例如：
```js
'\x41'; // 完全等同于 'A'
```

还可以用`\u####`表示一个`Unicode字符`：
```js
'\u4e2d\u6587'; // 完全等同于 '中文'
```
#### 多行字符串

用反引号\`...\`表示一个多行的字符串，可以替代重复使用`\n`
```js
`这是一个多行
字符串
啊哈哈哈
你看这个字符串它又长又..唔唔唔（捂嘴警告)`;
\\ 可以在浏览器中用 console.log(多行字符串)来检验该浏览器是否支持ES6这一语法
```
#### 将多个变量串联起来
用`+`号：
```js
var name = '小明';
var age = 20;
var message = '你好, ' + name + ', 你今年' + age + '岁了!';
\\ 这里的 “你好”，name变量，“你今年”，age变量，“岁了！”当作不同的字符串通过 +连到一起
alert(message);
```
ES6新增了一种模板字符串，表示方法和上面的多行字符串一样，但是它会**自动替换字符串中的变量**：
```js
var name = '小明';
var age = 20;
var message = `你好, ${name}, 你今年${age}岁了!`;
\\ 这里的文字字符串不需要单独引号出来
alert(message);
```

#### 对字符串的操作

 - 计算长度 `var.length;`

```js
 var s = 'Hello, world!';
 s.length; // 13
```
 - 获取字符串中指定位置内容 `var[位置]`

```js
 var s = 'Hello, world!';
s[0]; // 'H'
s[6]; // ' '
s[7]; // 'w'
s[12]; // '!'
s[13]; // undefined 超出范围的索引不会报错，但一律返回undefined
```
JavaScript为字符串提供了一些常用方法，注意，调用这些方法本身不会改变原有字符串的内容，而是返回一个**新字符串**：
 - 返回大写 `toUpperCase()`

```js
var s = 'Hello';
s.toUpperCase(); // 返回'HELLO'
```
 - 返回小写 `toLowerCase()`

```js
var s = 'Hello';
var lower = s.toLowerCase(); // 返回'hello'并赋值给变量lower
lower; // 'hello'
```
 - 指定字符串出现的位置 `indexOf()`

```js
var s = 'hello, world';
s.indexOf('world'); // 返回7，这是第7个字符开始的字符
s.indexOf('World'); // 没有找到指定的子串，返回-1
```
 - 返回指定索引区间的子串  `substring()`

```js
var s = 'hello, world'
s.substring(0, 5); // 从索引0开始到5（不包括5），返回'hello'
s.substring(7); // 从索引7开始到结束，返回'world'
```

---

### 数据类型——数组

#### 对数组的操作
赋值非常自由，可以接改变某个元素的值，也可以直接改变数组的长度。

##### slice

`slice()`就是对应`String`的`substring()`版本，它截取 Array 的部分元素，然后返回一个新的 Array：
```js
var arr = ['A', 'B', 'C', 'D', 'E', 'F', 'G'];
arr.slice(0, 3); // 从索引0开始，到索引3结束，但不包括索引3: ['A', 'B', 'C']
arr.slice(3); // 从索引3开始到结束: ['D', 'E', 'F', 'G']
```
注意到 `slice()`的起止参数包括**开始索引，不包括结束索引。**

如果不给`slice()`传递任何参数，它就会从头到尾截取所有元素。利用这一点，我们可以很容易地复制一个Array：
```js
var arr = ['A', 'B', 'C', 'D', 'E', 'F', 'G'];
var aCopy = arr.slice();
aCopy; // ['A', 'B', 'C', 'D', 'E', 'F', 'G']
aCopy === arr; // false
```
##### push和pop

`push()`向Array的末尾**添加**若干元素

`pop()`则把Array的最后一个元素**删除**掉：
```js
var arr = [1, 2];
arr.push('A', 'B'); // 返回Array新的长度: 4
arr; // [1, 2, 'A', 'B']
arr.pop(); // pop()返回'B'
arr; // [1, 2, 'A']
arr.pop(); // 空数组继续pop不会报错，而是返回undefined
arr; // []
```
##### unshift和shift

如果要往Array的**头部**添加若干元素，使用`unshift()方法`;

`shift()`方法则把Array的第一个元素删掉：
```js
var arr = [1, 2];
arr.unshift('A', 'B'); // 返回Array新的长度: 4
arr; // ['A', 'B', 1, 2]
arr.shift(); // 'A'
arr; // ['B', 1, 2]
arr.shift(); arr.shift(); arr.shift(); // 连续shift 3次
arr; // []
arr.shift(); // 空数组继续shift不会报错，而是返回undefined
arr; // []
```
##### sort

`sort()`可以对当前Array进行排序，它会直接修改当前Array的元素位置，直接调用时，按照默认顺序排序：
```js
var arr = ['B', 'C', 'A'];
arr.sort();
arr; // ['A', 'B', 'C']
```

##### splice

`splice()`方法是修改Array的“万能方法”，它可以从指定的索引开始删除若干元素，然后再从该位置添加若干元素：

`arr.splice(删除/添加开始的位置，删除数量，添加元素)`
```js
var arr = ['Microsoft', 'Apple', 'Yahoo', 'AOL', 'Excite', 'Oracle'];
// 从索引2开始删除3个元素,然后再添加两个元素:
arr.splice(2, 3, 'Google', 'Facebook'); // 返回删除的元素 ['Yahoo', 'AOL', 'Excite']
arr; // ['Microsoft', 'Apple', 'Google', 'Facebook', 'Oracle']

// 只删除,不添加:
arr.splice(2, 2); // ['Google', 'Facebook']
arr; // ['Microsoft', 'Apple', 'Oracle']

// 只添加,不删除:
arr.splice(2, 0, 'Google', 'Facebook'); // 返回[],因为没有删除任何元素
arr; // ['Microsoft', 'Apple', 'Google', 'Facebook', 'Oracle']
```
##### concat

`concat()`方法把当前的Array和另一个Array **连接**起来，并返回一个新的Array：
```js
var arr = ['A', 'B', 'C'];
var added = arr.concat([1, 2, 3]);
added; // ['A', 'B', 'C', 1, 2, 3]
arr; // ['A', 'B', 'C']
```

concat()方法可以接收任意个元素和Array，并且自动把Array拆开，然后全部添加到新的Array里：
```js
var arr = ['A', 'B', 'C'];
arr.concat(1, 2, [3, 4]); // ['A', 'B', 'C', 1, 2, 3, 4]
```

##### join

`join()` 方法是一个非常实用的方法，它把当前Array的每个元素都用指定的字符串连接起来，然后返回连接后的字符串：
```js
var arr = ['A', 'B', 'C', 1, 2, 3];
arr.join('-'); // 'A-B-C-1-2-3'
```
如果Array的元素不是字符串，将自动转换为字符串后再连接。

---
### 数据类型——对象
```
对象名{
属性名：属性值，
属性名2：属性值，属性
名3：属性值
}
```
对象的`属性`是通过 `.` 来调用的。

属性名一般不用特殊字符
