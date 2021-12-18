# 洛达什 _。camelCase()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-camelcase-method/](https://www.geeksforgeeks.org/lodash-_-camelcase-method/)

**_。camelCase()方法**用于将字符串转换为 camel case 字符串。字符串可以用空格、破折号或下划线分隔。

**语法:**

```
_.camelCase(string)

```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **字符串:**此参数保存需要转换为驼色大小写字符串的字符串。

**返回值:**此方法返回骆驼大小写字符串。

下面的例子说明了 Lodash _。JavaScript 中的 camelCase()方法:

**例 1:**

## java 描述语言

```
// Requiring the lodash library 
const _ = require('lodash'); 

// Use of _.camelCase() method
var str1 = _.camelCase("Geeks for Geeks");

// Printing the output 
console.log(str1);

// Use of _.camelCase() method
var str2 = _.camelCase("GFG-Geeks");

// Printing the output 
console.log(str2);
```

**输出:**

```
geeksForGeeks
gfgGeeks

```

**例 2:**

## java 描述语言

```
// Requiring the lodash library 
const _ = require('lodash'); 

// Use of _.camelCase() method
var str1 = _.camelCase("Geeks__for__Geeks");

// Printing the output 
console.log(str1);

// Use of _.camelCase() method
var str2 = _.camelCase("GFG--Geeks");

// Printing the output 
console.log(str2);
```

**输出:**

```
geeksForGeeks
gfgGeeks

```