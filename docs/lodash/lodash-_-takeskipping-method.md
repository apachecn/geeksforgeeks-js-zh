# 洛达什 _。takeSkipping()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-takeskipping-method/](https://www.geeksforgeeks.org/lodash-_-takeskipping-method/)

洛达什 T3**_。take skip()方法** 取一个数组和一个 skip 值(比如 n)，创建一个包含原数组每第 n 个元素的数组。

对于一个索引>= 0的第一个元素新数组总是与相同的第一个元素原始数组。

**语法:**

```
_.takeSkipping(array, skip_value)

```

**参数:**该方法取两个参数，如上所述，描述如下:

*   **数组:**要制作跳过数组的数组。
*   **skip_value:** 用于从原始数组制作 skip 数组的值。

**返回值:**这个方法返回一个新创建的跳过数组。

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装 lodash contrib 库。

**模块安装:**可以使用以下命令安装 Lodash contrib 库:

```
npm install lodash-contrib –save
```

**示例 1:** 在本例中，我们将使用此方法生成一个跳过数组。

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

// Array
var array = [1, 2, 3, 4, 6, 4, 3, 10];

// SkipValue
var skip = 2;

// Generating Array using takeSkipping() method
var arr = _.takeSkipping(array, skip);

console.log("Array : ", array);
console.log("Skip Value : ", skip);
console.log("Generated Array : ", arr);
```

**输出:**生成的跳过数组包含第(n+2)个索引元素。

```
Array :  [
  1, 2, 3, 4,
  6, 4, 3, 10
]
Skip Value :  2
Generated Array :  [ 1, 3, 6, 3 ]

```

**示例 2:** 该方法对于大于或小于数组大小的跳过值是安全的。

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

// Array
var array = [1, 2, 3, 4, 6, 4, 3, 10];

// SkipValue
var skip = 10;

// Generating Array using takeSkipping() method
var arr = _.takeSkipping(array, skip);

console.log("Array : ", array);
console.log("Skip Value : ", skip);
console.log("Generated Array : ", arr);
```

**输出:**生成的数组中只有第一个元素或第 0 个索引元素。

```
Array :  [
  1, 2, 3, 4,
  6, 4, 3, 10
]
Skip Value :  10
Generated Array :  [ 1 ]

```

**示例 3:** 对于负跳过值，它返回一个空数组。

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

// Array
var array = [1, 2, 3, 4, 6, 4, 3, 10];

// skipValue
var skip = -10;

// Generating Array using takeSkipping() method
var arr =_.takeSkipping(array, skip);

console.log("Array : ", array);
console.log("Skip Value : ", skip);
console.log("Generated Array : ", arr);
```

**输出:**

```
Array :  [
  1, 2, 3, 4,
  6, 4, 3, 10
]
Skip Value :  -10
Generated Array :  []

```