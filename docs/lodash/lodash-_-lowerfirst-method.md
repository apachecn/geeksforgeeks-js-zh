# 洛达什 _。lowerFirst()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-lowerfirst-method/](https://www.geeksforgeeks.org/lodash-_-lowerfirst-method/)

_。lowerFirst()方法用于将给定字符串的第一个字符转换为小写字符。

**语法:**

```
_.lowerFirst([string=''])

```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **String:** This parameter stores the string to be converted.

**返回值:**这个方法返回转换后的字符串。

**例 1:**

## Javascript

```
const _ = require('lodash'); 

var str1 = _.lowerFirst("GEEKS FOR GEEKS");
console.log(str1);

var str2 = _.lowerFirst("GFG--Geeks");
console.log(str2);
```

**输出:**

```
"gEEKS FOR GEEKS"
"gFG--Geeks"

```

**例二:**

## Javascript

```
const _ = require('lodash'); 

var str1 = _.lowerFirst("GEEKS__FOR__GEEKS");
console.log(str1);

var str2 = _.lowerFirst("G4G--geeks--GEEKS");
console.log(str2);

var str3 = _.lowerFirst("GEEKS-----FOR_____Geeks");
console.log(str3);
```

**输出:**

```
"gEEKS__FOR__GEEKS"
"g4G--geeks--GEEKS"
"gEEKS-----FOR_____Geeks"

```