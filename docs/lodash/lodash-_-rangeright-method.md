# 洛达什 _。rangeRight()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-rangeright-method/](https://www.geeksforgeeks.org/lodash-_-rangeright-method/)

Lodash 是一个工作在下划线. js 之上的 JavaScript 库，Lodash 有助于处理数组、字符串、对象、数字等。

**_。rangeRight()** 方法用于创建从给定的**起始**值到给定的但不包括给定的**结束**值的数字数组。它以降序填充这些值。如果指定了一个没有结束或步骤的负开始，则使用-1 的**步骤**值。如果没有指定**结束**，则设置为从**开始**开始，然后设置为 0。

**语法:**

```
_.rangeRight( start, end, step )
```

**参数:**该方法接受三个参数，如上所述，如下所述:

*   **start:** 是一个指定范围开始的数字。它是一个可选值。默认值为 0。
*   **end:** 是一个指定范围结束的数字。
*   **步:**是一个数字，指定范围内的值递增或递减的量。默认值为 1。

**返回值:**返回一个数组，数组中的数字范围按降序排列。

**例 1:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");            

// Using the _.rangeRight() method 
let range_arr = _.rangeRight(6); 

// Printing the output  
console.log(range_arr);
```

**输出:**

```
[5, 4, 3, 2, 1, 0]

```

**例 2:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");            

// Using the _.rangeRight() method
// with the step taken as 3
let range_arr = _.rangeRight(0,15,3); 

// Printing the output  
console.log(range_arr);
```

**输出:**

```
[12, 9, 6, 3, 0]

```

**例 3:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");            

// Using the _.rangeRight() method
// with the step taken as -2
let range_arr = _.rangeRight(0,-10,-2); 

// Printing the output  
console.log(range_arr);
```

**输出:**

```
[-8, -6, -4, -2, 0]

```