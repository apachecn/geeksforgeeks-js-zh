# 洛达什 _。findLast()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-findlast-method/](https://www.geeksforgeeks.org/lodash-_-findlast-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、集合、字符串、对象、数字等。

**_。findLast()方法**从右向左迭代集合中的元素。几乎和 _。find()方法。

**语法:**

```
_.findLast( collection, predicate, fromIndex )
```

**参数:**该方法接受三个参数，如上所述，如下所述:

*   **集合:**是方法迭代的集合。
*   **谓词:**是每次迭代调用的函数。
*   **fromIndex:** 是搜索开始的数组的索引。

**返回值:**这个方法返回匹配的元素，否则不定义。

**例 1:**

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var users = ([3, 4, 5, 6]);

// Using the _.findLast() method
let found_elem = _.findLast(users, function(n) {
  return n % 2 == 1;
});

// Printing the output 
console.log(found_elem);
```

**输出:**

```
5
```

**例 2:**

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var user1 = ([3, 4, 5, 6, 9, 1, 7]);
var user2 = ([24, 14, 55, 36, 76]);

// Using the _.findLast() method
let found_elem = _.findLast(user1, function(n) {
  return n % 2 == 0;
});
let found_elem2 = _.findLast(user2, function(n) {
  return n % 2 == 1;
});

// Printing the output 
console.log(found_elem);
console.log(found_elem2);
```

**输出:**

```
6
55
```

**例 3:**

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var user1 = ([3.5, 4.7, 5.8, 6.9, 9.4, 1.3, 7.2]);

// Using the _.findLast() method
let found_elem = _.findLast(user1, function(n) {
  return n % 2 == 1;
});

// Printing the output 
console.log(found_elem);
```

**输出:**

```
undefined
```