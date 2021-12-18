# 洛达什 _。minBy()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-minby-method/](https://www.geeksforgeeks.org/lodash-_-minby-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、字符串、对象、数字等。

**_。minBy()** **方法**用于通过使用迭代函数迭代数组中的每个元素来计算原始数组的最小值。几乎和 _。min()函数。

**语法:**

```
_.minBy( array, [iteratee = _.identity] )

```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **数组:**是方法迭代得到最小元素的数组。
*   **迭代:**是为数组中的每个元素调用的函数。

**返回值:**该方法返回最小元素。

**例 1:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Original array 
var arr = [{ 'n': 4 }, { 'n': 2 }, { 'n': 6 }];

// Use of _.minBy() method 
let min_val = 
  _.minBy(arr, function(o) { return o.n; }); 

// Printing the output  
console.log(min_val);
```

**输出:**

```
{ 'n': 2 }

```

**例 2:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Original array 
var arr = [{ 'n': 10 }, { 'n': 5 }, 
           { 'n': 3 }, { 'n': 12 }];

// Use of _.minBy() method 
let min_val = _.minBy(arr, 'n'); 

// Printing the output  
console.log(min_val);
```

**输出:**

```
{ 'n': 3 }

```