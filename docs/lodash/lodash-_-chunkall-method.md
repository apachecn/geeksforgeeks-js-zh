# 洛达什 _。chunkAll()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-chunkall-method/](https://www.geeksforgeeks.org/lodash-_-chunkall-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、字符串、对象、数字等。

**_。chunkAll()** **方法**是用来将给定的数组分成给定大小的小块。它是类似于的 _。chunk() 方法除了这个 方法永远不会从末尾掉短组块。

**语法:**

```
_.chunkAll( array, number )

```

或者

```
_.chunkAll( array, number, partitions )

```

**参数:**该方法取三个参数，如上所述，讨论如下:

*   **阵:**就是要拆分的阵。
*   **数字:**是要形成的组块的大小。
*   **分区:**它指定了如何从跳过的区域构建分区。这是一个可选参数。

**返回值:**这个方法返回一个分块数组。

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装 lodash-contrib 库。可以使用 **npm 安装 lodash-contrib–保存**来安装 lodash-contrib 库

**示例 1:** 在本例中，我们将对一个简单的数组进行分块。

## java 描述语言

```
// Defining lodash contrib variable
var _ = require('lodash-contrib'); 

// Array to be chunked
var arr = [2,2,3,5,6]

// Number that denotes the size
// of the chunks
var num = 3

// Using the _.chunkAll() method
var carr = _.chunkAll(arr, num); 

console.log("array  : ");
console.log(arr);
console.log("number : "); 
console.log(num); 
console.log("chunked array : ");
console.log(carr);
```

**输出:**

```
array  :
[ 2, 2, 3, 5, 6 ]
number :
3
chunked array :
[ [ 2, 2, 3 ], [ 5, 6 ] ]

```

**示例 2:** 在本例中，我们将使用可选参数来构建跳过的分区。

## java 描述语言

```
// Defining lodash contrib variable
var _ = require('lodash-contrib'); 

// Array to be chunked
var arr = [2,2,3,5,6]

// Number that denotes the size
// of the chunks
var num = 3

// Optional Arg
var opt = 4

// Using the _.chunkAll() method
carr = _.chunkAll(arr, num, opt);

console.log("array  : ");
console.log(arr);
console.log("number : "); 
console.log(num); 
console.log("chunked array : ");
console.log(carr);
```

**输出:**

```
array  :
[ 2, 2, 3, 5, 6 ]
number :
3
chunked array :
[ [ 2, 2, 3 ], [ 6 ] ]

```