# 下划线. js _。neg()方法

> 原文:[https://www.geeksforgeeks.org/underscore-js-_-neg-method/](https://www.geeksforgeeks.org/underscore-js-_-neg-method/)

**_。neg()** 方法返回一个与给定数字符号值相反的新数字。

**语法:**

```
_.neg( value );
```

**参数:**该方法取 n 个值对其进行运算。

**返回值:**该方法返回一个新的数字，其符号值与给定的数字相反。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。

可以使用 **npm 安装下划线-contrib–save 来安装下划线. js contrib 库。**

**例 1:**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var n  = _.neg( -1 );

console.log("Opposite sign value number is :", n);
```

**输出:**

```
Opposite sign value number is : 1
```

**例 2:**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var n  = _.neg( 1 );

console.log("Opposite sign value number is :", n);
```

**输出:**

```
Opposite sign value number is : -1
```

**例 3:**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var n  = _.neg( -3 );

console.log("Opposite sign value number is :", n);
```

**输出:**

```
Opposite sign value number is : 3
```

**例 4:**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var n  = _.neg( 6 );

console.log("Opposite sign value number is :", n);
```

**输出:**

```
Opposite sign value number is : -6
```