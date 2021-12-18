# 下划线. js _。neq()方法

> 原文:[https://www.geeksforgeeks.org/underscore-js-_-neq-method/](https://www.geeksforgeeks.org/underscore-js-_-neq-method/)

**_。neq()** 方法使用松散不等式(！=).因此，相应地返回一个布尔值。

**语法:**

```
_.neq( val1, val2, ..., valn );
```

**参数:**该方法取 n 个值对其进行运算。

**返回值:**这个方法返回一个布尔值。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。

可以使用 **npm 安装下划线-contrib–save 来安装下划线. js contrib 库。**

**例 1:**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var neq  = _.neq( 3, 1 );

console.log("Each arguments are not equal to previous one :", neq);
```

**输出:**

```
Each arguments are not equal to previous one : true
```

**例 2:**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var neq  = _.neq( 4, 4 );

console.log("Each arguments are not equal to previous one :", neq);
```

**输出:**

```
Each arguments are not equal to previous one : false
```

**例 3:**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var neq  = _.neq( 4, 2, 1 );

console.log("Each arguments are not equal to previous one :", neq);
```

**输出:**

```
Each arguments are not equal to previous one : true
```

**例 4:**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var neq  = _.neq( 2, 2, 2 );

console.log("Each arguments are not equal to previous one :", neq);
```

**输出:**

```
Each arguments are not equal to previous one : false
```