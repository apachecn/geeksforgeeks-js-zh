# 洛达什 _。takeWhile()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-takewhile-method/](https://www.geeksforgeeks.org/lodash-_-takewhile-method/)

_。taken 同时该方法用于创建一个数组切片，其中的元素是从开始处获取的。此外，这些元素一直被接受，直到谓词错误地返回。

**语法:**

```
_.takeWhile(array, [predicate=_.identity])

```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **Array:** This parameter stores the array to be queried.
*   **[predicate = _]. Identity]:** This parameter holds the function called in each iteration.

**返回值:**此方法用于返回数组的切片。

**示例 1:** 这里，const _ = require('lodash ')用于导入文件中的 lodash 库。

## JavaScript

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var users = [
  { 'user': 'jupiter',  'active': false },
  { 'user': 'mercury',    'active': false },
  { 'user': 'saturn', 'active': true }
];

// Use of _.takeWhile() 
// method
let gfg = _.takeWhile(users, function(o) { return !o.active; });

// Printing the output 
console.log(gfg);
```

**输出:**

```
[{ user: 'jupiter', active: false },
 {user: 'mercury', active: false}]

```

**例二:**

## JavaScript

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var users = [
  { 'user': 'jupiter',  'active': false },
  { 'user': 'mercury',    'active': false },
  { 'user': 'saturn', 'active': true }
];

// Use of _.takeWhile() 
// method
// The `_.matches` iteratee shorthand.

let gfg = _.takeWhile(users, { 'user': 'jupiter', 'active': false });

// Printing the output 
console.log(gfg);
```

**输出:**

```
[{ user: 'jupiter', active: false }]

```

**例三:**

## JavaScript

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var users = [
  { 'user': 'jupiter',  'active': false },
  { 'user': 'mercury',    'active': false },
  { 'user': 'saturn', 'active': true }
];

// Use of _.takeWhile() 
// method
// The `_.matchesProperty` iteratee shorthand.

let gfg = _.takeWhile(users, ['active', false]);

// Printing the output 
console.log(gfg);
```

**输出:**

```
[{ user: 'jupiter', active: false },
 {user: 'mercury', active: false}]

```

**例 4:**

## JavaScript

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var users = [
  { 'user': 'jupiter',  'active': false },
  { 'user': 'mercury',    'active': false },
  { 'user': 'saturn', 'active': true }
];

// Use of _.takeWhile() 
// method
// The `_.property` iteratee shorthand.

let gfg = _.takeWhile(users, 'active');

// Printing the output 
console.log(gfg);
```

**输出:**

```
[]

```

**注意:**这段代码在正常的 JavaScript 中无法工作，因为它需要安装库 lodash。