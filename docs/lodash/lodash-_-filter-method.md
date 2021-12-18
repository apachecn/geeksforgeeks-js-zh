# 洛达什 _。过滤器()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-filter-method/](https://www.geeksforgeeks.org/lodash-_-filter-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、集合、字符串、对象、数字等。

**_。filter()** 方法迭代集合的元素，返回所有元素的数组谓词返回 true。

**注意:**这个方法和 _。remove()方法，因为该方法返回一个新数组。

**语法:**

```
_.filter( collection, predicate )
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **集合:**此参数保存要迭代的集合。
*   **谓词:**此参数保存每次迭代调用的函数。

**返回值:**这个方法返回新的过滤数组。

**例 1:**

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var users = [
  { 'user': 'luv',
    'salary': 36000,
    'active': true },
  { 'user': 'kush', 
    'salary': 40000,
    'active': false }
];

// Using the _.filter() method
let filtered_array = _.filter(
    users, function(o) {
       return !o.active;
    }
);

// Printing the output 
console.log(filtered_array);
```

**输出:**

```
[ { user: 'kush', salary: 40000, active: false } ]
```

**例 2:**

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var users = [
  { 'user': 'luv',
    'salary': 36000,
    'active': true },
  { 'user': 'kush', 
    'salary': 40000,
    'active': false }
];

// Using the _.filter() method
// The `_.matches` iteratee shorthand
let filtered_array = _.filter(users, 
    { 'salary': 36000, 'active': true }
);

// Printing the output 
console.log(filtered_array);
```

**输出:**

```
[ { user: 'luv', salary: 36000, active: true } ]
```

**例 3:**

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var users = [
  { 'user': 'luv',
    'salary': 36000,
    'active': true },
  { 'user': 'kush', 
    'salary': 40000,
    'active': false }
];

// Using the _.filter() method
// The `_.matchesProperty` iteratee shorthand
let filtered_array =
  _.filter(users, ['active', false]);

// Printing the output 
console.log(filtered_array);
```

**输出:**

```
[ { user: 'kush', salary: 40000, active: false } ]
```

**例 4:**

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var users = [
  { 'user': 'luv',
    'salary': 36000,
    'active': true },
  { 'user': 'kush', 
    'salary': 40000,
    'active': false }
];

// Using the _.filter() method
// The `_.property` iteratee shorthand
let filtered_array =
  _.filter(users, 'active');

// Printing the output 
console.log(filtered_array);
```

**输出:**

```
[ { user: 'luv', salary: 36000, active: true } ]
```