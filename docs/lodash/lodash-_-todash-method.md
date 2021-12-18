# 洛达什 _。toDash()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-todash-method/](https://www.geeksforgeeks.org/lodash-_-todash-method/)

**洛达什 _。toDash()方法**用于将驼色大小写字符串转换为虚线字符串。

**语法:**

```
_.toDash( camelCaseString);

```

**参数:**该方法取一个参数，如上所述，如下所述:

*   **camel skestring:** This method takes a camelCaseString and converts it into a dotted string.

**返回值:**这个方法返回一个转换后的虚线字符串。

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装 lodash.js contrib 库。可以使用 **npm 安装 lodash-contrib** 来安装 Lodash.js contrib 库。

**例 1:**

## Javascript

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

var dashst  = _.toDash("geeksForGeeks"); 

console.log("The converted Dashed String is :", dashst);
```

**输出:**

```
The converted Dashed String is : geeks-for-geeks

```

**例二:**

## Javascript

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

var dashst  = _.toDash("aBC"); 

console.log("The converted Dashed String is :", dashst);
```

**输出:**

```
The converted Dashed String is : a-b-c

```