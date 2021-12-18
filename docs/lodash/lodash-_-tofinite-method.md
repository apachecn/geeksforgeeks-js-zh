# 洛达什 _。toFinite()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-tofinite-method/](https://www.geeksforgeeks.org/lodash-_-tofinite-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、字符串、对象、数字等。

**_。toFinite()** 方法用于将给定值转换为有限数。

**语法:**

```
_.toFinite( value )

```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **值:**此参数保存要转换的值。

**返回值:**此方法返回转换后的数字。

**例 1:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.toFinite() method 
console.log(_.toFinite(Number.MAX_VALUE)); 
console.log(_.toFinite(15.6));
```

**输出:**

```
1.7976931348623157e+308
15.6

```

**例 2:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.toFinite() method 
console.log(_.toFinite(void 0)); 
console.log(_.toFinite(Number.MIN_VALUE));
```

**输出:**

```
0
5e-324

```