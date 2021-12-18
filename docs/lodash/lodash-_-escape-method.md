# 洛达什 _。逸()法

> 原文:[https://www.geeksforgeeks.org/lodash-_-escape-method/](https://www.geeksforgeeks.org/lodash-_-escape-method/)

Lodash 是一个工作在下划线. js 之上的 JavaScript 库，Lodash 有助于处理数组、字符串、对象、数字等。

_。escape()方法用于将给定字符串的字符“&”、“”、“”、“””转换为它们对应的 HTML 实体。

**语法:**

```
_.escape([string=''])

```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **字符串:**此参数保存包含转义字符的字符串。

**返回值:**该方法返回转义字符串。

**例 1:**

## Javascript

```
const _ = require('lodash'); 

var str1 = _.escape("Geeks << for >> Geeks");
console.log(str1);

var str2 = _.escape("GFG && Geeks");
console.log(str2);
```

**输出:**

```
"Geeks &lt;&lt; for &gt;&gt; Geeks"
"GFG &amp;&amp; Geeks"

```

**例二:**

## Javascript

```
const _ = require('lodash'); 

var str1 = _.escape("Geeks & Geeks");
console.log(str1);

var str2 = _.escape("GFG '+' Geeks");
console.log(str2);

var str3 = _.escape("'Geeks'");
console.log(str3);
```

**输出:**

```
"Geeks &amp; Geeks"
"GFG &#30;+' Geeks"
"'Geeks'"

```