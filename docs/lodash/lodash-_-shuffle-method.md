# 洛达什 _。shuffle()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-shuffle-method/](https://www.geeksforgeeks.org/lodash-_-shuffle-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、集合、字符串、对象、数字等。

**_。shuffle()** 方法使用一个版本的 Fisher-Yates shuffle 算法从给定集合中创建一个洗牌值数组。

**语法:**

```
_.shuffle( collection )
```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **集合:**此参数保存要洗牌的集合。

**返回值:**该方法用于返回新的混洗数组。

**例 1:**

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var array = [2, 4, 6, 9, 10];

// Use of _.shuffle() method
let shuffled_array = _.shuffle(array);

// Printing the output 
console.log(shuffled_array);
```

**输出:**

```
[ 10, 9, 4, 2, 6 ]
```

**例 2:**

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var array = ['mon', 'tue', 'wed', 'thu', 'fri', 'sat', 'sun'];

// Use of _.shuffle() method
let shuffled_array = _.shuffle(array);

// Printing the output 
console.log(shuffled_array);
```

**输出:**

```
[ 'sat', 'wed', 'fri', 'sun', 'thu', 'mon',  'tue']
```