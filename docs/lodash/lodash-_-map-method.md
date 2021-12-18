# 洛达什 _。地图()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-map-method/](https://www.geeksforgeeks.org/lodash-_-map-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、集合、字符串、对象、数字等。

**_。map()** 方法通过迭代运行集合中的每个元素来创建一个值数组。有许多 lodash 方法被保护起来，作为像 _)这样的方法的迭代。every()，_。filter()，_。map()，_。mapValues()，_。拒绝()，和 _。一些()方法。

**语法:**

```
_.map( collection, iteratee )
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **集合:**此参数保存要迭代的集合。
*   **迭代:**此参数保存每次迭代调用的函数。

**返回值:**该方法返回新映射的数组。

**例 1:**

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var array = _.map([5, 18]);

// Use of _.map() method
let mapped_array = _.map(array, function square(n) {
  return n * n;
})

// Printing the output 
console.log(mapped_array);
```

**输出:**

```
[ 25, 324 ]
```

**例 2:**

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var array = _.map({ 'x': 14, 'y': 28 });

// Use of _.map() method
let mapped_array = _.map(array, function square(n) {
  return n * n;
})

// Printing the output 
console.log(mapped_array);
```

**输出:**

```
[ 196, 784 ]
```

**例 3:**

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var users = [
  { 'user': 'jonny' },
  { 'user': 'john' }
];

// Use of _.map() method
// The `_.property` iteratee shorthand
let mapped_array = _.map(users, 'user');

// Printing the output 
console.log(mapped_array);
```

**输出:**

```
[ 'jonny', 'john' ]
```