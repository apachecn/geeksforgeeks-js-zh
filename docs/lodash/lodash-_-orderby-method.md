# 洛达什 _。orderBy()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-orderby-method/](https://www.geeksforgeeks.org/lodash-_-orderby-method/)

Lodash 是一个工作在下划线. js 之上的 JavaScript 库。Lodash 有助于处理数组、集合、字符串、对象、数字等。_。orderBy()方法类似于 _。方法，除了它允许迭代的排序顺序作为排序依据。如果未指定顺序，则所有值都按升序排序，否则相应值的顺序指定“desc”为降序，或“asc”为升序排序。

**语法:**

```
_.orderBy(collection, iteratees, orders)
```

**参数:**该方法接受三个参数，如上所述，如下所述:

*   **Set:** This parameter stores the set to be iterated.
*   **Iteration:** This parameter stores the iteration to be sorted.
*   **Order:** This parameter stores the sort order of iteration.

**返回值:**这个方法返回新的排序数组。

**示例 1:** 这里，const _ = require('lodash ')用于导入文件中的 lodash 库。

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var users = [
  { 'patron': 'jonny',   'age': 48 },
  { 'patron': 'john', 'age': 34 },
  { 'patron': 'john',   'age': 40 },
  { 'patron': 'jonny', 'age': 36 }
];

// Use of _.orderBy() method
// Sort by `patron` in ascending order
// and by `age` in descending order

let gfg = _.orderBy(users, ['patron', 'age'], 
             ['asc', 'desc']);

// Printing the output 
console.log(gfg);
```

**输出:**

```
[
  { 'patron': 'john',   'age': 40 },
  { 'patron': 'john', 'age': 34 },
  { 'patron': 'jonny',   'age': 48 },
  { 'patron': 'jonny', 'age': 36 }
]

```

**例 2:**

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var users = [
  { 'employee': 'hunny',   'salary': 60000 },
  { 'employee': 'munny', 'salary': 40000 },
  { 'employee': 'hunny',   'salary': 55000 },
  { 'employee': 'munny', 'salary': 36000 }
];

// Use of _.orderBy() method
// Sort by `employee` in ascending order
// and by `salary` in descending order

let gfg = _.orderBy(users, ['employee', 
           'salary'], ['asc', 'desc']);

// Printing the output 
console.log(gfg);
```

**输出:**

```
[
  { 'employee': 'hunny',   'salary': 60000 },
  { 'employee': 'hunny', 'salary': 55000 },
  { 'employee': 'munny',   'salary': 40000 },
  { 'employee': 'munny', 'salary': 36000 }
]

```

**注意:**这段代码在正常的 JavaScript 中无法工作，因为它需要安装库 lodash。