# 下划线. js _。mod()功能

> 原文:[https://www.geeksforgeeks.org/underscore-js-_-mod-method/](https://www.geeksforgeeks.org/underscore-js-_-mod-method/)

**_。mod()** 函数返回给定被除数除以给定除数的余数。

**语法:**

```
_.mod( dividend, divisor );
```

**参数:**

*   **股息:**计算 mod 的给定股息。
*   **除数:**给定用于计算模数的除数。

**返回值:**该方法从给定的参数返回计算的模数。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。

可以使用 **npm 安装下划线-contrib–save 来安装下划线. js contrib 库。**

**例 1:**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var mod  = _.mod( 24, 5 );

console.log("The Modulus is :", mod);
```

**输出:**

```
The Modulus is : 4
```

**例 2:**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var mod  = _.mod( 120, 25 );

console.log("The Modulus is :", mod);
```

**输出:**

```
The Modulus is : 20
```

**例 3:**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var mod  = _.mod( 12, 1 );

console.log("The Modulus is :", mod);
```

**输出:**

```
The Modulus is : 0
```