# 下划线. js _。chunkAll()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-chunkall-method/](https://www.geeksforgeeks.org/underscore-js-_-chunkall-method/)

**_。chunkAll()** **法**类似于 _。chunk() 方法除了下面那个， _。chunkAll() 方法永远不会从最后掉短块。制作组块和分块数组也需要一个数组和一个数字。

**语法:**

```
_.chunkAll(array, number);
```

或者

```
_.chunkAll(array, number, partitions);
```

**参数:**

*   **阵:**待拆分的阵。
*   **数字:**要形成的块的大小。
*   **分区(可选):**它表示如何从跳过的区域构建分区。

**返回值:**这个方法返回一个分块数组。

**注意:** 这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。 可以使用 **npm 安装下划线-contrib–保存**来安装下划线. js contrib 库

**示例 1:** 在本例中，我们将对一个简单的数组进行分块。

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Array
var arr = [2, 2, 3, 5, 6]

// Number
var num = 3

// Making Chunked array
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
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Array
var arr = [2, 2, 3, 5, 6]

// Number
var num = 3

// Optional Arg
var opt = 4

// Making Chunked array
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