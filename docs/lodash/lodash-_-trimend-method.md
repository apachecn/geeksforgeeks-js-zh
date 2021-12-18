# 洛达什 _。trimEnd()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-trimend-method/](https://www.geeksforgeeks.org/lodash-_-trimend-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、字符串、对象、数字等。

**_。trimEnd()方法**用于从给定字符串的末尾移除尾随空格或指定字符。

**语法:**

```
_.trimEnd( string, chars )

```

**参数:** 该方法接受两个参数，如上所述，描述如下:

*   **字符串:**是需要修剪的字符串。默认值为空字符串。
*   **字符:**这是一组必须从字符串中删除的字符。这是一个可选参数。默认值是空白。

**返回值:**该方法返回修剪后的字符串。

**例 1:**

## Javascript

```
// Defining Lodash variable 
const _ = require('lodash'); 

// The string to trim
var str = "   Geeks-for-Geeks   ";

// Using _.trimEnd() method
console.log(_.trimEnd(str));
```

**输出:**

```
"   Geeks-for-Geeks"

```

**例二:**

## Javascript

```
// Defining Lodash variable 
const _ = require('lodash'); 

// The string to trim
var str = "----GeeksforGeeks----";

// Using _.trimEnd() method
// with specific characters to trim
console.log(_.trimEnd(str, "-"))
```

**输出:**

```
"----GeeksforGeeks"

```