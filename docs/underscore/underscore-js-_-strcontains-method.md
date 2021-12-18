# 下划线. js _。strContains()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-strcontains-method/](https://www.geeksforgeeks.org/underscore-js-_-strcontains-method/)

**_。方法检查给定的字符串是否包含搜索到的字符串。**

**语法:**

```
_.strContains( string, searched_str);

```

**参数:**该方法接受两个参数，如上所述，如下所述

*   **字符串:**该方法取要搜索搜索字符串的字符串。
*   **search _ str:**该方法取一个要搜索的字符串。

**返回值:**这个方法 r 返回一个布尔值。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。

可以使用 **npm 安装下划线-contrib–save 来安装下划线. js contrib 库。**

**例 1:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var bool  = _.strContains("GeeksforGeeks","Geeks");

console.log("The String contains the searched String : ",bool);
```

**输出:**

```
The String contains the searched String :  true

```

**例 2:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var bool  = _.strContains("abc","d");

console.log("The String contains the searched String : ",bool);
```

**输出:**

```
The String contains the searched String :  false

```

**例 3:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var bool  = _.strContains("abc","a");

console.log("The String contains the searched String : ",bool);
```

**输出:**

```
The String contains the searched String :  true

```