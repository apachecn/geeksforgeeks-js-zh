# 洛达什 _。一些()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-some-method/](https://www.geeksforgeeks.org/lodash-_-some-method/)

Lodash 是一个工作在下划线. js 之上的 JavaScript 库。Lodash 有助于处理数组、集合、字符串、对象、数字等。

_。some()方法用于检查集合的任何元素的谓词是否返回 true。一旦谓词返回 true，迭代就停止。

**语法:**

```
_.some(collection, predicate)
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **集合:**此参数保存要迭代的集合。
*   **谓词:**此参数保存每次迭代调用的函数，并通过三个参数(值、索引|键、集合)调用。

**返回值:**如果有任何元素通过谓词检查，则该方法返回 true，否则返回 false。

**示例 1:** 这里，const _ = require('lodash ')用于导入文件中的 lodash 库。

## java 描述语言

```
// Requiring the lodash library
const _ = require("lodash");

// Original array and use of _.some() method
var gfg = _.some([null, 0, 'yes', false], Boolean);

// Printing the output
console.log(gfg);
```

**输出:**

```
true
```

**例 2:**

## java 描述语言

```
// Requiring the lodash library
const _ = require("lodash");

// Original array
var object = [
  { 'obj': 'moto', 'active': true },
  { 'obj': 'lenovo',   'active': false } ];

// Use of _.some() method
// The `_.matches` iteratee shorthand

let gfg = _.some(object, { 'obj': 'moto', 'active': false });

// Printing the output
console.log(gfg);
```

**输出:**

```
false
```

**例 3:**

## java 描述语言

```
// Requiring the lodash library
const _ = require("lodash");

// Original array

var object = [
  { 'obj': 'moto', 'active': true },
  { 'obj': 'lenovo',   'active': false } ];

// Use of _.some() method
// The `_.matchesProperty` iteratee shorthand

let gfg = _.some(object, ['active', false]);

// Printing the output
console.log(gfg);
```

**输出:**

```
true
```

**例 4:**

## java 描述语言

```
// Requiring the lodash library
const _ = require("lodash");

// Original array
var object = [
  { 'obj': 'moto', 'active': true },
  { 'obj': 'lenovo',   'active': false } ];

// Use of _.some() method
// The `_.property` iteratee shorthand

let gfg = _.some(object, 'active');

// Printing the output
console.log(gfg);
```

**输出:**

```
true
```

**注意:**这段代码在正常的 JavaScript 中无法工作，因为它需要安装库 lodash。