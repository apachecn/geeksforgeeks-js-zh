# 洛达什 _。groupBy()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-groupby-method/](https://www.geeksforgeeks.org/lodash-_-groupby-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、集合、字符串、对象、数字等。

**_。groupBy()方法**创建一个对象，该对象由通过迭代函数运行集合的每个元素的结果生成的键组成。分组值的顺序由它们在集合中出现的顺序决定。每个键的对应值也是负责生成该键的元素数组。

**语法:**

```
_.groupBy( collection, iteratee )
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **集合:**是方法迭代的集合。
*   **迭代:**是为数组中的每个元素调用的函数。

**返回值:**该方法返回合成的聚合对象。

**例 1:**

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var users = ([6.5, 4.12, 6.8, 5.4]);

// Using the _.groupBy() method
let grouped_data = _.groupBy(users, Math.floor )

console.log(grouped_data);
```

**输出:**

```
{ '4': [ 4.12 ], '5': [ 5.4 ], '6':[ 6.5, 6.8 ] }
```

**例 2:**

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var users = (['eight', 'nine', 'four', 'seven']);

// Using of _.groupBy() method
// with the `_.property` iteratee shorthand 
let grouped_data = _.groupBy(users, 'length')

console.log(grouped_data);
```

**输出:**

```
{ '4': [ 'nine', 'four' ], '5': [ 'eight', 'seven' ]}
```

**例 3:**

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var users = (['one', 'two', 'three', 'four']);
var obj = ([ 3.1, 1.2, 3.3 ]);

// Using the _.groupBy() method
// with the `_.property` iteratee shorthand 
let grouped_data = _.groupBy(users, 'length')
let grouped_data2 = _.groupBy(obj, Math.floor)

// Printing the output 
console.log(grouped_data, grouped_data2);
```

**输出:**

```
{ '3': [ 'one', 'two' ], '4': [ 'four' ], '5': [ 'three' ] } 
{ '1': [ 1.2 ], '3': [ 3.1, 3.3 ] }
```