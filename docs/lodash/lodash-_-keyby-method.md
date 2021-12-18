# 洛达什 _。keyBy()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-keyby-method/](https://www.geeksforgeeks.org/lodash-_-keyby-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、集合、字符串、对象、数字等。

**_。方法创建一个对象，该对象由通过迭代运行集合的每个元素的结果生成的键组成。每个键的对应值是负责生成该键的最后一个元素。**

**语法:**

```
_.keyBy( collection, iteratee )
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **集合:**此参数保存要迭代的集合。
*   **迭代:**该参数保存迭代转换键。

**返回值:**该方法返回合成的聚合对象。

**例 1:**

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var array = [
  { 'dir': 'left', 'code': 89 },
  { 'dir': 'right', 'code': 71 }
];

// Use of _.keyBy() method
let keyby_array = _.keyBy(array, 'dir');

// Printing the output 
console.log(keyby_array);
```

**输出:**

```
{ 'left': { 'dir': 'left', 'code': 89 }, 
'right': { 'dir': 'right', 'code': 71 } }
```

**例 2:**

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var array = [
  { 'dir': 'left', 'code': 89 },
  { 'dir': 'right', 'code': 71 }
];

// Use of _.keyBy() method
let keyby_array = _.keyBy(array, function(o) {
  return String.fromCharCode(o.code);
});

// Printing the output 
console.log(keyby_array);
```

**输出:**

```
{ 'Y': { 'dir': 'left', 'code': 89 }, 
'G': { 'dir': 'right', 'code': 71 } }
```