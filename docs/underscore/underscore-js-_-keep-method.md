# 下划线. js _。保持()方法

> 原文:[https://www.geeksforgeeks.org/underscore-js-_-keep-method/](https://www.geeksforgeeks.org/underscore-js-_-keep-method/)

**_。keep()方法**接受一个数组和一个函数，因此返回一个生成的数组，该数组只保留基于函数条件的真值。

**语法:**

```
_.keep(array, function)
```

**参数:**

*   **数组:**创建 keep 数组的给定数组。
*   **函数:**包含要保留元素的条件的函数。

**返回值:**这个方法返回一个新创建的数组。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。

可以使用 **npm 安装下划线-contrib–save 来安装下划线. js contrib 库。**

**示例 1:** 在本例中，我们将通过保留所有正值来创建一个数组。

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 
// Array
var array = [-1, -21, -43, 34, 12, -1];
// Getting keep array using keep() method
var k_array =_.keep(array, function(x){
    if(x>0){
        return x;
    }
});
console.log("Original Array : ", array);
console.log("Generated keep Array : ", k_array);
```

**输出:**

```
Original Array :  [ -1, -21, -43, 34, 12, -1 ]
Generated keep Array :  [ 34, 12 ]
```

**示例 2:** 在本例中，我们将通过保留所有负值来创建一个数组。

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 
// Array
var array = [-1, -21, -43, 34, 12, -1];
// Getting keep array using keep() method
var k_array =_.keep(array, function(x){
    if(x < 0){
        return x;
    }
});
console.log("Original Array : ", array);
console.log("Generated keep Array : ", k_array);
```

**输出:**

```
Original Array :  [ -1, -21, -43, 34, 12, -1 ]
Generated keep Array :  [ -1, -21, -43, -1 ]
```

**示例 3:** 在本例中，我们将通过保持所有 5 的倍数来创建一个数组。

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 
// Array
var array = [-1, -25, -43, 10, 125, -1];
// Getting keep array using keep() method
var k_array =_.keep(array, function(x){
    if(x % 5 == 0){
        return x;
    }
});
console.log("Original Array : ", array);
console.log("Generated keep Array : ", k_array);
```

**输出:**

```
Original Array :  [ -1, -25, -43, 10, 125, -1 ]
Generated keep Array :  [ -25, 10, 125 ]
```