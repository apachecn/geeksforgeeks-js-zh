# 洛达什 _。isNumber()函数

> 原文:[https://www.geeksforgeeks.org/lodash-_-isnumber-function/](https://www.geeksforgeeks.org/lodash-_-isnumber-function/)

**Lodash** 是一个工作在下划线. js 之上的 JavaScript 库，Lodash 有助于处理数组、字符串、对象、数字等。

**_。isNumber()** 方法用于查找给定值参数是否为数字。如果给定值是一个数字，则返回真值，否则返回假值。

**语法:**

```
_.isNumber(value)
```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **值:**该参数保存要检查的值。

**返回值:**如果值为数字，则该方法返回 true，否则返回 false。

**示例 1:** 这里，const _ = require('lodash ')用于将 lodash 库导入文件。

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.isNumber() method 

console.log(_.isNumber(10)); 
console.log(_.isNumber('GeeksforGeeks')); 
console.log(_.isNumber(15.675));
```

**输出:**

```
true
false
true
```

**例二:**

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.isNumber()  
// method 

console.log(_.isNumber(true));
console.log(_.isNumber(Number.MIN_VALUE)); 
console.log(_.isNumber(Infinity));
console.log(_.isNumber('3'));
```

**输出:**

```
false
true
true
false
```