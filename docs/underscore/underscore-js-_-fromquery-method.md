# 下划线. js _。fromQuery()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-fromquery-method/](https://www.geeksforgeeks.org/underscore-js-_-fromquery-method/)

**_。fromQuery()** 方法用于将给定的 URL 查询字符串转换为等效的 JavaScript 对象。

**语法:**

```
_.fromQuery( URL_Query);

```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **URL _ query:** This method uses URL query string for conversion.

**返回值:**这个方法 r 返回等价的 JavaScript 对象。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。

可以使用 **npm 安装下划线-contrib–save 来安装下划线. js contrib 库。**

**例 1:**

## Javascript

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var s  = _.fromQuery("https://example.com/path/to/page?name=ferret&color=purple");

console.log("The generated JavaScript Object is : ",s);
```

**输出:**

```
The generated JavaScript Object is :  
{ 'https://example.com/path/to/page?name': 'ferret', color: 'purple' }

```

**例二:**

## Javascript

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var s  = _.fromQuery("https://practice.geeksforgeeks.org/courses/?ref=gfg_header");

console.log("The generated JavaScript Object is : ",s);
```

**输出:**

```
The generated JavaScript Object is :  
{ 'https://practice.geeksforgeeks.org/courses/?ref': 'gfg_header' }

```