# 洛达什 _。减少()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-reduce-method/](https://www.geeksforgeeks.org/lodash-_-reduce-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、集合、字符串、对象、数字等。
The _。reduce()方法将集合缩减为值，该值是通过迭代运行集合中每个元素的累积结果，其中每个连续的调用都被提供上一个调用的返回值。如果没有给定累加器，则集合的第一个元素用作初始值。有许多 lodash 方法被保护起来，作为像 _)这样的方法的迭代。减少，_。reduceRight 和 _.transform。

**语法:**

```
_.reduce(collection, iteratee, accumulator)

```

**参数:**该方法接受三个参数，如上所述，如下所述:

*   **集合:**此参数保存要迭代的集合。
*   **迭代:**此参数保存每次迭代调用的函数。
*   **累加器:**此参数保存初始值。

**返回值:**此方法返回累计值。

**示例 1:** 这里，const _ = require('lodash ')用于导入文件中的 lodash 库。

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var users = [ 1, 2, 3, 4 ];

// Use of _.reduce() method

let gfg = _.reduce(users, function(sum, n) {
  return sum + n;
}, 0);

// Printing the output 
console.log(gfg);
```

**输出:**

```
10

```

**例 2:**

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var users = { 'p': 2, 'q': 3, 'r':2, 's': 2  }

// Use of _.reduce() method

let gfg = _.reduce(users, function(result, value, key) {
  (result[value] || (result[value] = [])).push(key);
  return result;
}, {});

// Printing the output 
console.log(gfg);
```

**输出:**

```
{ '2': ['p', 'r', 's'], '3': ['q'] }

```

**注意:**这段代码在正常的 JavaScript 中无法工作，因为它需要安装库 lodash。