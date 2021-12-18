# 洛达什 _。invokeMap()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-invokemap-method/](https://www.geeksforgeeks.org/lodash-_-invokemap-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、集合、字符串、对象、数字等。

**_。invokeMap()** 方法调用位于**集合**中每个元素的给定**路径**的方法，并返回每个被调用方法的结果数组。可以使用**参数**为每个调用的方法提供额外的参数。给定的**路径**也可以是绑定到集合中每个元素的函数。

**语法:**

```
_.invokeMap( collection, path, args )
```

**参数:**该方法接受三个参数，如上所述，如下所述:

*   **集合:**此参数保存必须迭代的集合。
*   **路径:**此参数保存每次迭代要调用的方法或调用的函数的路径。
*   **参数:**该参数保存调用每个方法的参数。

**返回值:**该方法返回结果数组。

**例 1:**

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
let obj = [[6, 2, 8], [2, 1, 0]];

// Using the _.invokeMap() method
let gfg1 = _.invokeMap(obj, 'sort');

// Printing the output 
console.log(gfg1);
```

**输出:**

```
[ [ 2, 6, 8], [ 0, 1, 2 ] ]
```

**例 2:**

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
let obj = [628, 210];

// Using the _.invokeMap() method 
let gfg1 = _.invokeMap(obj, String.prototype.split, '');

// Printing the output 
console.log(gfg1);
```

**输出:**

```
[ [ '6', '2', '8'], [ '2', '1', '0' ] ]
```

**例 3:**

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
let obj = ['srqp', 'tuvw'];
let obj1 = [ ['c', 'b', 'a'], ['f', 'e', 'd'] ];

// Using the _.invokeMap() method
let gfg = _.invokeMap(obj, String.prototype.split, '');
let gfg1 = _.invokeMap(obj1, 'sort');

// Printing the output 
console.log(gfg, gfg1);
```

**输出:**

```
[ [ 's', 'r', 'q', 'p'], [ 't', 'u', 'v', 'w' ] ]
[ [ 'a', 'b', 'c'], [ 'd', 'e', 'f' ] ]
```