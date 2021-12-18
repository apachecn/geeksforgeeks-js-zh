# 洛达什 _。sortBy()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-sortby-method/](https://www.geeksforgeeks.org/lodash-_-sortby-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、集合、字符串、对象、数字等。

_。sortBy()方法创建一个元素数组，该数组按照每次迭代运行集合中每个元素的结果按升序排序。此外，该方法执行稳定的排序，这意味着它保留了相等元素的原始排序顺序。

**语法:**

```
_.sortBy(collection, iteratees)
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **集合:**此参数保存要迭代的集合。
*   **迭代:**此参数保存要排序的迭代，并使用一个参数(值)调用。

**返回值:**此方法用于返回新的排序数组。

**示例 1:** 这里，const _ = require('lodash ')用于导入文件中的 lodash 库。

## JavaScript

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var object = [
  { 'obj': 'moto', 'price': 19999 },
  { 'obj': 'oppo', 'price': 18999 },
  { 'obj': 'moto', 'price': 17999 },
  { 'obj': 'oppo', 'price': 15999 } ];

// Use of _.sortBy() method
let gfg = _.sortBy(object, 
    [function(o) { return o.obj; }]);

// Printing the output 
console.log(gfg);
```

**输出:**

```
[
  { 'obj': 'moto', 'price': 19999 },
  { 'obj': 'moto', 'price': 17999 },
  { 'obj': 'oppo', 'price': 18999 },
  { 'obj': 'oppo', 'price': 15999 }
]

```

**例二:**

## JavaScript

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var object = [
  { 'obj': 'moto', 'price': 19999 },
  { 'obj': 'oppo', 'price': 18999 },
  { 'obj': 'moto', 'price': 17999 },
  { 'obj': 'oppo', 'price': 15999 } ];

// Use of _.sortBy() method
let gfg = _.sortBy(object, ['obj', 'price']);

// Printing the output 
console.log(gfg);
```

**输出:**

```
[
  { 'obj': 'moto', 'price': 17999 },
  { 'obj': 'moto', 'price': 19999 },
  { 'obj': 'oppo', 'price': 15999 },
  { 'obj': 'oppo', 'price': 18999 } 
]

```

**注意:**这段代码在正常的 JavaScript 中无法工作，因为它需要安装库 lodash。