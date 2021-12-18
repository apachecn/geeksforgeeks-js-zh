# 下划线. js _。toDash()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-todash-method/](https://www.geeksforgeeks.org/underscore-js-_-todash-method/)

**_。toDash()** 方法用于将 camel case 字符串转换为虚线字符串。

**语法:**

```
_.toDash( camelCaseString);
```

**参数:**

*   **todash:** This method needs a camel Case String to be converted.

**返回值:**这个方法返回一个转换后的虚线字符串。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。

可以使用 **npm 安装下划线-contrib–save 来安装下划线. js contrib 库。**

**例 1:**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var dashst  = _.toDash("geeksForGeeks");

console.log("The converted Dashed String is :",dashst);
```

**输出:**

```
The converted Dashed String is : geeks-for-geeks
```

**例 2:**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var dashst  = _.toDash("aBC");

console.log("The converted Dashed String is :",dashst);
```

**输出:**

```
The converted Dashed String is : a-b-c
```