# 洛达什 _。最小()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-min-method/](https://www.geeksforgeeks.org/lodash-_-min-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、字符串、对象、数字等。

**_。min()** **法**用于从数组中寻找最小元素。如果数组为空，则返回 undefined。

**语法:**

```
_.min( array )

```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **数组:**是方法迭代得到最小元素的数组。

**返回值:**这个方法从数组中返回最小元素。

**例 1:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.min() method 
let min_val = _.min([]); 

// Printing the output  
console.log(min_val);
```

**输出:**

```
undefined

```

**例 2:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.min() method 
let min_val = _.min([15, 7, 38, 46, 82]); 

// Printing the output  
console.log(min_val);
```

**输出:**

```
7

```

**例 3:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.min() method 
let min_val = _.min([-15, 7, 38, -46, -82]); 

// Printing the output  
console.log(min_val);
```

**输出:**

```
-82

```