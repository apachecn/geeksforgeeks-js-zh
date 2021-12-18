# 洛达什 _。toSafeInteger()方法

> 原文:[https://www . geeksforgeeks . org/lo dash-_-to safe integer-method/](https://www.geeksforgeeks.org/lodash-_-tosafeinteger-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、字符串、对象、数字等。

**_。方法用于将该值转换为安全整数。**

**语法:**

```
_.toSafeInteger( value )

```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **值:**此参数保存要转换的值。

**返回值:**该方法返回转换后的整数。

**例 1:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.toSafeInteger() method 
console.log(_.toSafeInteger(15.6)); 
console.log(_.toSafeInteger('15.6'));
```

**输出:**

```
15
15

```

**例 2:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.toSafeInteger() method 
console.log(_.toSafeInteger(Number.MIN_VALUE)); 
console.log(_.toSafeInteger(Number.MAX_VALUE));
```

**输出:**

```
0
9007199254740991

```