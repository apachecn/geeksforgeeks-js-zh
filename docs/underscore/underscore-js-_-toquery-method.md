# 下划线. js _。toQuery()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-toquery-method/](https://www.geeksforgeeks.org/underscore-js-_-toquery-method/)

**_。toQuery()** 方法接受一个对象，并将其转换为等价的 URL 查询字符串。

**语法:**

```
_.toQuery( Object);

```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **Object:** This method needs an object for conversion.

**返回值:**这个方法 r 返回等价的网址查询字符串。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。

可以使用 **npm 安装下划线-contrib–save 来安装下划线. js contrib 库。**

**例 1:**

## Javascript

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var s  = _.toQuery({ name: 'gfg', color: 'green' });

console.log("The generated URL Query String is : ",s);
```

**输出:**

```
The generated URL Query String is :  name=gfg&color=green

```

**例二:**

## Javascript

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var s  = _.toQuery({ 'https://practice.geeksforgeeks.org/courses/?ref': 'gfg_header' });

console.log("The generated URL Query String is : ",s);
```

**输出:**

```
The generated URL Query String is : 
https%3A%2F%2Fpractice.geeksforgeeks.org%2Fcourses%2F%3Fref=gfg_header

```