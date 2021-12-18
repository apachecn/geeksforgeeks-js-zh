# 洛达什 _。均值()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-mean-method/](https://www.geeksforgeeks.org/lodash-_-mean-method/)

**Lodash** 是一个工作在下划线. js 之上的 JavaScript 库，Lodash 有助于处理数组、字符串、对象、数字等。

**_。mean()** 方法用于求数组中值的平均值。

**语法:**

```
_.mean( array )
```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **数组:**是方法迭代得到所有值的平均值的数组。

**返回值:**此方法返回数组中值的平均值。

**例 1:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.mean()  
// method 
let mean_val = _.mean([15, 7, 38, 46, 82]); 

// Printing the output  
console.log(mean_val);
```

**输出:**

```
37.6
```

**例 2:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.mean()  
// method 
let mean_val = _.mean([2, 3, 4, 6, 7, 8]); 

// Printing the output  
console.log(mean_val);
```

**输出:**

```
5
```

**例 3:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.mean()  
// method 
let mean_val = _.mean([10, -4, -6, 8, 12]); 

// Printing the output  
console.log(mean_val);
```

**输出:**

```
4
```