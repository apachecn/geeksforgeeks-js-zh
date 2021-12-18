# 洛达什 _。overSome()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-oversome-method/](https://www.geeksforgeeks.org/lodash-_-oversome-method/)

洛达什 **_。overSome()** 方法用于创建一个函数，该函数检查当使用接收到的参数调用时，是否有任何谓词返回 truthy。

**语法:**

```
_.overSome( predicates )

```

**参数:**该方法接受一个参数，如上所述，如下所述:

*   **谓词**:这是要调用的谓词。

**返回值:**这个方法返回一个新的函数。

**例 1:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");              

// Use of _.overSome() method 
var func = _.overSome([Boolean, isFinite]);

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
true
false
```

**例 2:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");              

// Use of _.overSome() method 
var func = _.overSome([Math.min,  Math.max]);

// Saving the result
let gfg = func(2, 4, -6, 8);

// Printing the output  
console.log(gfg);
```

**输出:**

```
true

```