# 洛达什 _。flatMap()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-flatmap-method/](https://www.geeksforgeeks.org/lodash-_-flatmap-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、集合、字符串、对象、数字等。
The _。flatMap()方法通过迭代和展平映射结果来运行集合中的每个元素，从而创建一个展平的值数组。

**语法:**

```
_.flatMap(collection, iteratee)
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **集合:**此参数保存要迭代的集合。
*   **迭代:**此参数保存每次迭代调用的函数。

**返回值:**该方法返回新的展平数组。

**示例 1:** 这里，const _ = require('lodash ')用于导入文件中的 lodash 库。

## java 描述语言

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var user1 = ([35, 47, 58, 69, 94, 13, 72]);

// Use of _.flatMap() method
let gfg1 = _.flatMap(user1, function duplicate(n) {
  return [n, n];
})

// Printing the output 
console.log(gfg1);
```

**输出:**

```
[
  35, 35, 47, 47, 58, 58, 
  69, 69, 94, 94, 13, 13,
  72, 72
]

```

**例 2:**

## java 描述语言

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var user1 = ([3.5, 4.7, 5.8, 6.9, 9.4, 1.3, 7.2]);
var user2 = ([3, 4, 5, 9, 9, 1, 7]);

// Use of _.flatMap() method
let gfg1 = _.flatMap(user1, function duplicate(n) {
  return [n, n];
})

let gfg2 = _.flatMap(user2, function duplicate(n) {
  return [n, n];
})

// Printing the output 
console.log(gfg1);
console.log(gfg2);
```

**输出:**

```
[
  3.5, 3.5, 4.7, 4.7, 5.8, 5.8, 
  6.9, 6.9, 9.4, 9.4, 1.3, 1.3,
  7.2, 7.2
]
[
  3, 3, 4, 4, 5, 5,
  9, 9, 9, 9, 1, 1,
  7, 7
]

```

**注意:**这段代码在正常的 JavaScript 中无法工作，因为它需要安装库 lodash。