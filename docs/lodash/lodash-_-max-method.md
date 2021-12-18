# 洛达什 _。最大()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-max-method/](https://www.geeksforgeeks.org/lodash-_-max-method/)

**Lodash** 是一个工作在下划线. js 之上的 JavaScript 库，Lodash 有助于处理数组、字符串、对象、数字等。

**_。max()** **法**用于从数组中寻找最大元素。如果数组为空，则返回 undefined。

**语法:**

```
_.max( array )
```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **数组:**是方法迭代得到最大元素的数组。

**返回值:**这个方法从数组中返回最大元素。

**例 1:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.max() method 
let max_val = _.max([]); 

// Printing the output  
console.log(max_val);
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

// Use of _.max() method 
let max_val = _.max([15, 7, 38, 46, 82]); 

// Printing the output  
console.log(max_val);
```

**输出:**

```
82
```

**例 3:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.max() method 
let max_val = _.max([-15, 7, 38, -46, -82]); 

// Printing the output  
console.log(max_val);
```

**输出:**

```
38
```