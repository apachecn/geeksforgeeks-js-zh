# 洛达什 _。strContains()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-strcontains-method/](https://www.geeksforgeeks.org/lodash-_-strcontains-method/)

**洛达什 _。strContains()方法**检查给定的字符串是否包含搜索到的字符串，并返回相应的布尔值。

**语法:**

```
_.strContains( string, searched_str);

```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **字符串:**该方法取要搜索搜索字符串的字符串。
*   **search _ str:**该方法取一个要搜索的字符串。

**返回值:**这个方法返回一个布尔值。

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装 lodash.js contrib 库。可以使用 **npm 安装 Lodash.js contrib 库-保存**。

**例 1:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

var bool  = _.strContains("GeeksforGeeks", "Geeks"); 

console.log("The String contains the "
    + "searched String : ", bool);
```

**输出:**

```
The String contains the searched String : true

```

**例 2:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

var bool  = _.strContains("abc", "d"); 

console.log("The String contains the "
    + "searched String : ", bool);
```

**输出:**

```
The String contains the searched String : false

```

**例 3:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

var bool  = _.strContains("abc", "a"); 

console.log("The String contains the "
    + "searched String : ", bool);
```

**输出:**

```
The String contains the searched String : true

```