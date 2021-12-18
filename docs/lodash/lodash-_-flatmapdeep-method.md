# 洛达什 _。flatMapDeep()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-flatmapdeep-method/](https://www.geeksforgeeks.org/lodash-_-flatmapdeep-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、集合、字符串、对象、数字等。

**_。flatMapDeep()** 方法通过迭代函数运行给定集合中的每个元素来创建一个展平的值数组，并递归展平映射的结果。它类似于 _。flatMap()方法。

**语法:**

```
_.flatMapDeep( collection, iteratee )
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **集合:**是要迭代的集合。
*   **迭代:**是每次迭代调用的函数。

**返回值:**该方法返回新的展平数组。

**例 1:**

```
// Requiring the lodash library 
const _ = require("lodash");

// Original array 
var users = (['aaa', 'bbb', 'ccc', 
              'ddd', 'eee', 'fff']);

// Using the _.flatMapDeep() method
let flat_map =
  _.flatMapDeep(users,
    function duplicate(n) {
      return [[[n, n]]];
  }
)

// Printing the output 
console.log(flat_map);
```

**输出:**

```
[
  'aaa', 'aaa', 'bbb', 'bbb',
  'ccc', 'ccc', 'ddd', 'ddd',
  'eee', 'eee'
]
```

**例 2:**

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var user1 = ([1, 2, 3, 4, 5, 6, 7]);
var user2 = (['a', 'b', 'c', 'd', 'e']);

// Using the _.flatMapDeep() method
let flat_map1 =
  _.flatMapDeep(user1,
    function makePattern(n) {
      return [[[n, n + "->"]]];
  }
)

let flat_map2 =
  _.flatMapDeep(user2,
    function makePattern(n) {
      return [[["<-" + n, n]]];
  }
)

// Printing the output 
console.log(flat_map1);
console.log(flat_map2);
```

**输出:**

```
[
  1, 1->, 2, 2->, 3, 3->,
  4, 4->, 5, 5->, 6, 6->,
  7, 7->
]
[
  '<-a', 'a', <-'b', 'b',
  '<-c', 'c', '<-d', 'd',
  '<-e', 'e'
]
```