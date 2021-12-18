# 洛达什 _。fromQuery()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-fromquery-method/](https://www.geeksforgeeks.org/lodash-_-fromquery-method/)

**洛达什 _。fromQuery()方法**用于将给定的 URL 查询字符串转换为等价的 JavaScript 对象。

**语法:**

```
_.fromQuery( URL_Query);
```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **网址 _ 查询:**该方法取一个网址查询字符串转换成 Java Script 语言对象。

**返回值:**这个方法返回等价的 JavaScript 对象。

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装 lodash.js contrib 库。可以使用 **npm 安装 Lodash.js contrib 库-保存**。

**例 1:**

## Javascript

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

var s  = _.fromQuery(
"https://geeksforgeeks.org/path/to/page?name=ferret&color=purple"); 

console.log("The generated JavaScript Object is : ", s);
```

**输出:**

```
The generated JavaScript Object is :
Object {
color: "purple" ,
https://geeksforgeeks.org/path/to/page?name: "ferret"
}

```

**例二:**

## Javascript

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

var s  = _.fromQuery(
"https://practice.geeksforgeeks.org/courses/?ref=gfg_header");

console.log("The generated JavaScript Object is : ", s);
```

**输出:**

```
The generated JavaScript Object is :
Object {https://practice.geeksforgeeks.org/courses/?ref: "gfg_header"}

```