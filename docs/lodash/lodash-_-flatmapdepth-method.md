# 洛达什 _。flatMapDepth()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-flatmapdepth-method/](https://www.geeksforgeeks.org/lodash-_-flatmapdepth-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、集合、字符串、对象、数字等。

**_。flatMapDepth()** 方法通过迭代函数运行给定集合中的每个元素来创建一个扁平的值数组。它递归地将映射结果展平到给定的深度值。它类似于 _。flatMap()方法。

**语法:**

```
_.flatMapDepth( collection, iteratee, depth )
```

**参数:**该方法接受三个参数，如上所述，如下所述:

*   **集合:**是要迭代的集合。
*   **迭代:**是每次迭代调用的函数。
*   **深度:**是指定最大递归深度的数字。这是一个可选参数。默认值为 1。

**返回值:**该方法返回新的展平数组。

**例 1:**

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var users = ([3, 4]);

// Using the _.flatMapDepth() method
let flat_map = _.flatMapDepth(users, duplicate, 2 )
function duplicate(n) {
  return [[[n, n]]];
}

// Printing the output 
console.log(flat_map);
```

**输出:**

```
[ [ 3, 3 ], [ 4, 4 ] ]
```

**例 2:**

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var users = (['q', 'r', 't', 'u']);

// Using the _.flatMapDepth() method
let flat_map = _.flatMapDepth(users, duplicate, 2 )
function duplicate(n) {
  return [[[n, n]]];
}

// Printing the output 
console.log(flat_map);
```

**输出:**

```
[ [ 'q', 'q' ], [ 'r', 'r' ], [ 't', 't' ], ['u', 'u' ] ]
```