# 下划线. js _。lt()方法

> 原文:[https://www.geeksforgeeks.org/underscore-js-_-lt-method/](https://www.geeksforgeeks.org/underscore-js-_-lt-method/)

**_。lt()** 方法检查每个参数是否小于其下一个参数。

**语法:**

```
_.lt( val1, val2, ..., valn );
```

**参数:**该方法取 n 个值对其进行运算。

**返回值:**这个方法返回一个布尔值。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。

可以使用 **npm 安装下划线-contrib–save 来安装下划线. js contrib 库。**

**例 1:**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 
var lesser  = _.lt(1, 4);
console.log("Each argument is lesser than its next argument :", lesser);
```

**输出:**

```
Each argument is lesser than its next argument : true
```

**例 2:**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 
var lesser  = _.lt(1, 4, 9);
console.log("Each argument is lesser than its next argument :", lesser);
```

**输出:**

```
Each argument is lesser than its next argument : true
```

**例 3:**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 
var lesser  = _.lt(1, 4, 4);
console.log("Each argument is lesser than its next argument :", lesser);
```

**输出:**

```
Each argument is lesser than its next argument : false
```