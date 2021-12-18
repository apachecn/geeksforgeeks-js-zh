# 下划线. js _。编织()方法

> 原文:[https://www.geeksforgeeks.org/underscore-js-_-weave-method/](https://www.geeksforgeeks.org/underscore-js-_-weave-method/)

****_。weave()方法** 取两个数组，返回一个两个数组编织在一起的数组。**

****注:**阵从返回 **_。编织()**方法将编织至最短数组，其余数组值均与相同。**

****语法:****

```
_.weave(array1, array2) 
```

****参数:****

*   ****数组 1:** 第一个数组。**
*   ****数组 2:** 第二个数组。**

****返回值:**这个方法返回一个由数组 1 和数组 2 组成的编织数组。**

****注意:** 这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。 可以使用 **npm 安装下划线-contrib-save 来安装下划线. js contrib 库。****

****示例 1:** 在本例中，我们将生成一个数组 1 和数组 2 大小相同的编织数组。**

## **java 描述语言**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Array1
var array1 = [1, 2, 3, 4];

// Array2
var array2 = [5, 6, 7, 8]

// Generating Array using weave() method
var arr =_.weave(array1, array2);
console.log("Array1 : ", array1);
console.log("Array2 : ", array2);
console.log("Woven Array : ", arr);
```

****输出:****

```
Array1 :  [ 1, 2, 3, 4 ]
Array2 :  [ 5, 6, 7, 8 ]
woven Array :  [
  1, 5, 2, 6,
  3, 7, 4, 8
] 
```

****例 2:** 当数组大小为 1 时<数组大小为 2**

## **java 描述语言**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Array1
var array1 = [1, 2];

// Array2
var array2 = [5, 6, 7, 8]

// Generating Array using weave() method
var arr =_.weave(array1, array2);
console.log("Array1 : ", array1);
console.log("Array2 : ", array2);
console.log("Woven Array : ", arr);
```

****输出:****

```
Array1 :  [ 1, 2 ]
Array2 :  [ 5, 6, 7, 8 ]
Woven Array :  [ 1, 5, 2, 6, 7, 8 ]
```

****例 3:** 当数组的大小 1 >数组的大小 2**

## **java 描述语言**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

// Array1
var array1 = [1, 2, 3, 4];

// Array2
var array2 = [5, 6]

// Generating Array using weave() method
var arr =_.weave(array1, array2);
console.log("Array1 : ", array1);
console.log("Array2 : ", array2);
console.log("Woven Array : ", arr);
```

****输出:****

```
Array1 :  [ 1, 2, 3, 4 ]
Array2 :  [ 5, 6 ]
Woven Array :  [ 1, 5, 2, 6, 3, 4 ]
```