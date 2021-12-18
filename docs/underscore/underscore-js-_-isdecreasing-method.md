# 下划线. js _。isDecreasing()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-is decreleasing-method/](https://www.geeksforgeeks.org/underscore-js-_-isdecreasing-method/)

**_。方法检查参数是否是单调递减的值，或者每个参数是否小于前一个参数。**

**语法:**

```
_.isDecreasing(val1,val2,...,valn);

```

**参数:**该方法 n 个值检查递减顺序。

**返回值:**该方法返回一个布尔值(如果给定值在减少，则返回真，否则返回假)。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。

可以使用 **npm 安装下划线-contrib–save 来安装下划线. js contrib 库。**

**例 1:** 方法返回真。

## Javascript

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 
// Checking
console.log("The Value is Decreasing : " +_.isDecreasing(3,2,1));
```

**输出:**

```
The Value is Decreasing : true

```

**例 2:** 方法返回假。

## Javascript

```
// Defining underscore contrib variable

var _ = require('underscore-contrib');

// Checking

console.log("The Value is Decreasing : " +_.isDecreasing(3,2,1,2));
```

**输出:**

```
The Value is Decreasing : false
```