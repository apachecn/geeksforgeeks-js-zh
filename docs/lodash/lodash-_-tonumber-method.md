# Lodash _。强调 no()方法〔t1〕

> 哎哎哎::1230【https://www . geeksforgeeks . org/LOD ash-_-强调 no-method/

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、字符串、对象、数字等。

**_。toNumber()** 方法用于将给定值转换为数字。

**语法:**

```
_.toNumber( value )

```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **值:**此参数保存要转换的值。

**返回值:**此方法返回转换后的数字。

**例 1:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.toNumber() method 
console.log(_.toNumber(15.6)); 
console.log(_.toNumber('15.6'));
```

**输出:**

```
15.6
15.6

```

**例 2:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.toNumber() method 
console.log(_.toNumber(Number.MIN_VALUE)); 
console.log(_.toNumber(Number.MAX_VALUE));
```

**输出:**

```
5e-324
1.7976931348623157e+308

```