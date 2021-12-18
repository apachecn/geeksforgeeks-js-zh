# 洛达什 _。范围()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-range-method/](https://www.geeksforgeeks.org/lodash-_-range-method/)

Lodash 是一个工作在下划线. js 之上的 JavaScript 库，Lodash 有助于处理数组、字符串、对象、数字等。

**_。range()** 方法用于创建从给定的**起始**值到但不包括**结束**值的数字数组。如果指定了负的开始值而没有结束或步骤，则使用-1 的**步骤**。如果没有指定**结束**，则设置为从**开始**开始，然后设置为 0。

**语法:**

```
_.range( start, end, step )
```

**参数:**该方法接受三个参数，如上所述，如下所述:

*   **start:** 是一个指定范围开始的数字。它是一个可选值。默认值为 0。
*   **end:** 是一个指定范围结束的数字。
*   **步:**是一个数字，指定范围内的值递增或递减的量。默认值为 1。

**返回值:**返回给定数字范围的数组。

**例 1:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");            

// Using the _.range() method 
let range_arr = _.range(5); 

// Printing the output  
console.log(range_arr);
```

**输出:**

```
[0, 1, 2, 3, 4]

```

**例 2:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");            

// Using the _.range() method
// with the step taken as 2
let range_arr = _.range(0,10,2); 

// Printing the output  
console.log(range_arr);
```

**输出:**

```
[0, 2, 4, 6, 8]

```

**例 3:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");            

// Using the _.range() method
// with the step taken as -2
let range_arr = _.range(-1,-11,-2); 

// Printing the output  
console.log(range_arr);
```

**输出:**

```
[-1, -3, -5, -7, -9]

```