# Lodash _。isJSON()方法〔t1〕

> 原文:[https://www.geeksforgeeks.org/lodash-_-isjson-method/](https://www.geeksforgeeks.org/lodash-_-isjson-method/)

**洛达什 _。isJSON()方法**检查给定值是否为有效的 JSON，并返回相应的布尔值。

**语法:**

```
_.isJSON( value );
```

**参数:**该方法取上述单参数，描述如下:

*   **值:**要检查 JSON 的给定值。

**返回值:**如果给定值为有效 JSON，则该方法返回布尔值 true，否则返回 false。

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装 lodash.js contrib 库。可以使用 **npm 安装 lodash-contrib** 来安装 Lodash.js contrib 库。

**例 1:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

// Checking for _.isJSON() method
console.log("The Value is JSON : " +_.isJSON( 
'{"GeeksforGeeks" : "A Computer Science portal for Geeks"}'));
```

**输出:**

```
The Value is JSON : true
```

**例 2:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

// Checking for _.isJSON() method
console.log("The Value is JSON : " +_.isJSON( 
{GeeksforGeeks : "A Computer Science portal for Geeks"}));
```

**输出:**

```
The Value is JSON : false
```

**例 3:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

// Checking for _.isJSON() method
console.log("The Value is JSON : " + _.isJSON(["gfg"]));
```

**输出:**

```
The Value is JSON : false
```