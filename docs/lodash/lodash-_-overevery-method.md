# 洛达什 _。overEvery()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-overevery-method/](https://www.geeksforgeeks.org/lodash-_-overevery-method/)

洛达什 **_。over throw**方法用于检查当使用函数接收的参数调用时，所有谓词是否返回真值。

**语法:**

```
_.overEvery(predicates)
```

**参数:**该方法接受一个参数，如上所述，如下所述:

*   **谓词:**要调用的谓词。

**返回:**此方法返回新函数。

**例 1:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");              

// Use of _.overEvery() method 
var func = _.overEvery([Math.min,  Math.max]);

// Saving the result
let gfg = func(2, 4, -6, 8);

// Printing the output  
console.log(gfg);
```

**输出:**

```
true

```

**例 2:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");              

// Use of _.overEvery() method 
var func = _.overEvery([Boolean, isFinite]);

// Saving the result
let gfg1 = func(10);
let gfg2 = func(-5);
let gfg3 = func(null);
let gfg4 = func(NaN);

// Printing the output  
console.log(gfg1); 
console.log(gfg2); 
console.log(gfg3); 
console.log(gfg4);
```

**输出:**

```
true
true
false
false

```