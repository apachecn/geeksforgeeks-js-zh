# 洛达什 _。nthArg()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-ntharg-method/](https://www.geeksforgeeks.org/lodash-_-ntharg-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、字符串、对象、数字等。

洛达什 **_。第 n 个参数()**方法创建一个函数，获取索引 n 处的参数，如果 n 为负，则返回末尾的第 n 个参数。

**语法:**

```
_.nthArg(n)
```

**参数:**该方法接受一个参数，如上所述，如下所述:

*   **n:** 要返回的参数的索引。

**返回:**返回新的通过函数。

**例 1:**

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");              

// Use of _.nthArg() method 
var func = _.nthArg(1);

let gfg = func('www','geeks','for','geeks');

// Printing the output  
console.log(gfg);
```

**输出:**

```
geeks

```

**例二:**

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");              

// Use of _.nthArg() method 
var func = _.nthArg(-4);

let gfg = func('www','geeks','for','geeks');

// Printing the output  
console.log(gfg);
```

**输出:**

```
www

```