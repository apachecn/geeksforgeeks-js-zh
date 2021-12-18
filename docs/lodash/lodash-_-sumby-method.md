# 洛达什 _。sumBy()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-sumby-method/](https://www.geeksforgeeks.org/lodash-_-sumby-method/)

**Lodash** 是一个工作在下划线. js 之上的 JavaScript 库，Lodash 有助于处理数组、字符串、对象、数字等。

**_。sumBy()** 方法用于通过使用迭代函数迭代数组中的每个元素来计算原始数组的和。几乎和 _。sum()方法。

**语法:**

```
_.sumBy(array, [iteratee = _.identity])
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **数组:**此参数保存要迭代的数组。
*   **【迭代= _。identity]:** 此参数保存每个元素调用的迭代。

**返回值:**此方法返回总和。

**示例 1:** 这里，const _ = require('lodash ')用于将 lodash 库导入文件。

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Original array 
var arr = [{ 'n': 4 }, { 'n': 2 }, { 'n': 6 }];

// Use of _.sumBy()  
// method 
let gfg = _.sumBy(arr, function(o) { return o.n; }); 

// Printing the output  
console.log(gfg);
```

**输出:**

```
12
```

**例 2:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Original array 
var arr = [{ 'n': 10 }, { 'n': 5 }, { 'n': 3 }, { 'n': 12 }];

// Use of _.sumBy()  
// method 
let gfg = _.sumBy(arr, 'n'); 

// Printing the output  
console.log(gfg);
```

**输出:**

```
30
```