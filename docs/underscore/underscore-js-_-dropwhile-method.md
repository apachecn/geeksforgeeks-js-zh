# 下划线. js _。dropWhile()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-dropwhile-method/](https://www.geeksforgeeks.org/underscore-js-_-dropwhile-method/)

****_。dropWhile()方法** 接受一个数组和一个函数，并因此返回一个数组，其中元素是从原始数组中删除的，函数返回真。**

****注意:**值被删除，直到函数返回 false，在 false 值之后，原始值不会发生变化。**

****语法:****

```
_.dropWhile(array, function) 
```

****参数:**该方法接受两个参数，如上所述，如下所述:**

*   ****数组:**创建删除数组的给定数组。**
*   ****函数:**包含要删除元素的条件的函数。**

****返回值:**这个方法返回一个新创建的数组。**

****注意:** 这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。**

**下划线. js contrib 库可以使用安装 **npm 安装下划线-contrib。****

****示例 1:** 在本例中，我们将创建一个删除所有正值的数组。**

## **java 描述语言**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 
// Array
var array = [11, 21, 43, 34, 12, -1];
// Getting dropped array using dropWhile() method
var d_array =_.dropWhile(array, function(x){
    return x > 0;
});
console.log("Array : ", array);
console.log("Dropped Array : ", d_array);
```

****输出:****

```
Array :  [ 11, 21, 43, 34, 12, -1 ]
Dropped Array :  [ -1 ] 
```

****示例 2:** 在本例中，我们将创建一个删除所有负值的数组。**

## **java 描述语言**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 
// Array
var array = [-1, -21, -43, 34, 12, -1];
// Getting dropped array using dropWhile() method
var d_array =_.dropWhile(array, function(x){
    return x < 0;
});
console.log("Array : ", array);
console.log("Dropped Array : ", d_array);
```

****输出:**负值下降，直到正值出现。**

```
Array :  [ -1, -21, -43, 34, 12, -1 ]
Dropped Array :  [ 34, 12, -1 ] 
```

****示例 3:** 在本例中，我们将创建一个数组，其中删除了 0 个值，直到函数返回 false。**

## **java 描述语言**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 
// Array
var array = [0, 0, 0, 0, 0, -1, -21, -43, 34, 12, -1];
// Getting dropped array using dropWhile() method
var d_array =_.dropWhile(array, function(x){
    return x == 0;
});
console.log("Array : ", array);
console.log("Dropped Array : ", d_array);
```

****输出:****

```
Array :  [
   0,   0,   0,  0,  0,
  -1, -21, -43, 34, 12,
  -1
]
Dropped Array :  [ -1, -21, -43, 34, 12, -1 ] 
```