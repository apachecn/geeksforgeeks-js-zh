# 洛达什 _。总和()法

> 原文:[https://www.geeksforgeeks.org/lodash-_-sum-method/](https://www.geeksforgeeks.org/lodash-_-sum-method/)

**Lodash** 是一个工作在下划线. js 之上的 JavaScript 库，Lodash 有助于处理数组、字符串、对象、数字等。

**_。sum()** 方法用于求数组中值的和。

**语法:**

```
_.sum(array)
```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **数组:**此参数保存要迭代的数组。

**返回值:**此方法返回数组中值的总和。

**示例 1:** 这里，const _ = require('lodash ')用于将 lodash 库导入文件。

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.sum () method 
let gfg = _.sum([5, 10, 15, 20, 25]); 

// Printing the output  
console.log(gfg);
```

**输出:**

```
75
```

**例二:**

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.sum () method 
let gfg = _.sum([8, -12, -13, 30, 45]); 

// Printing the output  
console.log(gfg);
```

**输出:**

```
58
```