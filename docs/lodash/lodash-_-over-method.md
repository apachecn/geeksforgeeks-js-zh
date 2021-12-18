# 洛达什 _。over()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-over-method/](https://www.geeksforgeeks.org/lodash-_-over-method/)

洛达什 **_。over()** 方法用于创建一个函数，该函数使用接收到的参数调用迭代并返回结果。

**语法:**

```
_.over(iteratees)
```

**参数:**该方法接受一个参数，如上所述，如下所述:

*   **迭代:**要调用的迭代。

**返回:**这个方法返回一个新的函数。

**例 1:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");              

// Use of _.over() method 
var func = _.over([Boolean, isFinite]);

// Saving the result
let gfg1 = func('10');
let gfg2 = func('-5');
let gfg3 = func('null');
let gfg4 = func('NaN');

// Printing the output  
console.log(gfg1); 
console.log(gfg2); 
console.log(gfg3); 
console.log(gfg4);
```

**输出:**

```
[true, true]
[true, true]
[true, false]
[true, false]

```

**例 2:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");              

// Use of _.over() method 
var func = _.over([Math.min,  Math.max]);

// Saving the result
let gfg = func(5, 10, -5, 20);

// Printing the output  
console.log(gfg);
```

**输出:**

```
[-5, 20]

```