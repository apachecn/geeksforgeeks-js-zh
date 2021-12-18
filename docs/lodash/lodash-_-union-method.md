# 洛达什 _。联合()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-union-method/](https://www.geeksforgeeks.org/lodash-_-union-method/)

**_。union()** 方法用于获取 n 个数组，并从所有给定数组中按顺序创建一个唯一值数组，使用 SameValueZero 进行相等比较。

**语法:**

```
_.union(*arrays)
```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **Array:** This parameter stores the array to be checked.

**返回值:**此方法用于返回新的组合值数组。

**示例 1:** 这里，const _ = require('lodash ')用于导入文件中的 lodash 库。

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.union() method 
let gfg = _.union([20, 12], [8, 15, 6]); 

// Printing the output  
console.log(gfg)
```

**输出:**

```
[20, 12, 8, 15, 6]
```

**例二:**

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash"); 

// Use of _.union() method 
let gfg = _.union([1, 2, 3],
                  [3, 4, 5], 
                  [6, 2, 7]); 

// Printing the output  
console.log(gfg)
```

**输出:**

```
[1, 2, 3, 4, 5, 6, 7]
```