# 洛达什 _。maxBy()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-maxby-method/](https://www.geeksforgeeks.org/lodash-_-maxby-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、字符串、对象、数字等。

**_。maxBy()** **方法**用于通过使用迭代函数迭代数组中的每个元素来计算原始数组的最大值。几乎和 _。max()函数。

**语法:**

```
_.maxBy( array, [iteratee = _.identity] )

```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **数组:**是方法迭代得到最大元素的数组。
*   **迭代:**是为数组中的每个元素调用的函数。

**返回值:**此方法返回最大元素。

**例 1:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Original array 
var arr = [{ 'n': 4 }, { 'n': 2 }, { 'n': 6 }];

// Use of _.maxBy() method 
let max_obj = _.maxBy(arr, function(o) { return o.n; }); 

// Printing the output  
console.log(max_obj);
```

**输出:**

```
{ 'n': 6 }

```

**例 2:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Original array 
var arr = [{ 'n': 10 }, { 'n': 5 }, 
           { 'n': 3 }, { 'n': 12 }];

// Use of _.maxBy() method 
let max_obj = _.maxBy(arr, 'n'); 

// Printing the output  
console.log(max_obj);
```

**输出:**

```
{ 'n': 12 }

```