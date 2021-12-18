# 洛达什 _。toInteger()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-tointeger-method/](https://www.geeksforgeeks.org/lodash-_-tointeger-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、字符串、对象、数字等。

**_。toInteger()** 方法用于将给定值转换为整数。

**语法:**

```
_.toInteger( value )

```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **值:**此参数保存要转换的值。

**返回值:**该方法返回转换后的整数。

**例 1:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.toInteger() method 
console.log(_.toInteger(void 0)); 
console.log(_.toInteger(15.6));
```

**输出:**

```
0
15

```

**例 2:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.toInteger() method 
console.log(_.toInteger(Number.MIN_VALUE)); 
console.log(_.toInteger(Number.MAX_VALUE));
```

**输出:**

```
0
1.7976931348623157e+308

```