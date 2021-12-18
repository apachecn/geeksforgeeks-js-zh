# 洛达什 _。分区()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-partition-method/](https://www.geeksforgeeks.org/lodash-_-partition-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、集合、字符串、对象、数字等。
The _。partition()方法创建一个分成两组的元素数组，第一组包含元素谓词返回 true，第二组包含元素谓词返回 false。

**语法:**

```
_.partition(collection, predicate)
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **集合:**此参数保存要迭代的集合。
*   **谓词:**此参数保存每次迭代调用的函数，并且用一个参数(值)调用

**返回值:**这个方法返回分组元素的数组。

**示例 1:** 这里，const _ = require('lodash ')用于导入文件中的 lodash 库。

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var users = [
  { 'customer': 'john',  'age': 26, 'active': false },
  { 'customer': 'jonny',    'age': 34, 'active': true },
  { 'customer': 'johnson', 'age': 12,  'active': false }
];

// Use of _.partition() method

let gfg = _.partition(users, function(o) { return 
o.active; });

// Printing the output 
console.log(gfg);
```

**输出:**

```
[
 [ { customer: 'jonny', age: 34, active: true },
   { customer: 'john', age: 26, active: false },
   { customer: 'johnson', age: 12, active: false }
  ]
]

```

**例 2:**

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var users = [
  { 'customer': 'john',  'age': 26, 'active': false },
  { 'customer': 'jonny',    'age': 34, 'active': true },
  { 'customer': 'johnson', 'age': 12,  'active': false }
];

// Use of _.partition() method
// The `_.matches` iteratee shorthand

let gfg = _.partition(users, { 'age': 12, 'active': false 
});

// Printing the output 
console.log(gfg);
```

**输出:**

```
[
 [ { customer: 'johnson', age: 12, active: false } ],
 [ { customer: 'john', age: 26, active: false },
   { customer: 'jonny', age: 34, active: true }
  ]
]

```

**例 3:**

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var users = [
  { 'customer': 'john',  'age': 26, 'active': false },
  { 'customer': 'jonny',    'age': 34, 'active': true },
  { 'customer': 'johnson', 'age': 12,  'active': false }
];

// Use of _.partition() method
// The `_.matchesProperty` iteratee shorthand

let gfg = _.partition(users, ['active', false]);

// Printing the output 
console.log(gfg);
```

**输出:**

```
[
 [ { customer: 'john', age: 26, active: false },
   { customer: 'johnson', age: 12, active: false } ],
 [ { customer: 'jonny', age: 34, active: true }
  ]
]

```

**例 4:**

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var users = [
  { 'customer': 'john',  'age': 26, 'active': false },
  { 'customer': 'jonny',    'age': 34, 'active': true },
  { 'customer': 'johnson', 'age': 12,  'active': false }
];

// Use of _.partition() method
// The `_.matches` iteratee shorthand

let gfg = _.partition(users, { 'age': 12, 'active': false 
});

// Printing the output 
console.log(gfg);
```

**输出:**

```
[
 [ { customer: 'johnson', age: 12, active: false } ],
 [ { customer: 'jonny', age: 34, active: true },
   { customer: 'john', age: 26, active: false } ]
]

```

**注意:**这段代码在正常的 JavaScript 中无法工作，因为它需要安装库 lodash。