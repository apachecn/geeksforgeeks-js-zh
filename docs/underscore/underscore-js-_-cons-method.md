# 下划线. js _。cons()方法

> 原文:[https://www.geeksforgeeks.org/underscore-js-_-cons-method/](https://www.geeksforgeeks.org/underscore-js-_-cons-method/)

**_。cons()方法**用于构造一个新的数组，取某个元素放在另一个数组或元素的前面。

**语法:**

```
_.cons(element, Array_or_element);
```

**参数:**

*   **元素:**是放在前面构造新数组的元素。
*   **Array_or_element:** 是用来构造数组的第二个参数。

**返回值:**这个方法返回一个新构造的数组。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。

可以使用 **npm 安装下划线-contrib–保存**来安装下划线. js contrib 库

**示例 1:** 在本例中，我们将使用这种方法，通过在前面放置一个元素来简单地构建一个新数组。

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 
// Element
var element = 0
// Array
var arr2 = [4, 5, 5]
// Constructing array
carr = _.cons(element, arr2);
console.log("element  : ");
console.log(element);
console.log("array2 : "); 
console.log(arr2); 
console.log("Constructed array : ");
console.log(carr);
```

**输出:**

```
element  :
0
array2 :
[ 4, 5, 5 ]
Constructed array :
[ 0, 4, 5, 5 ]

```

**例 2:** 这个元素也是以数组作为第一个参数。

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 
// Array1
var arr1 = [0]
// Array2
var arr2 = [4, 5, 5]
// Constructing array
carr = _.cons(arr1, arr2);
console.log("Array1  : ");
console.log(arr1);
console.log("Array2 : "); 
console.log(arr2); 
console.log("Constructed array : ");
console.log(carr);
```

**输出:**在本例中，第一个阵列作为子阵列出现

```
element  :
[ 0 ]
array2 :
[ 4, 5, 5 ]
Constructed array :
[ [ 0 ], 4, 5, 5 ]

```

**示例 3:** 在本例中，我们将使用参数构造一个新数组。

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 
function f() { return _.cons(0, arguments) }
console.log("Constructed array : ");
console.log(f(1, 2, 3));
```

**输出:**

```
Constructed array :
[ 0, 1, 2, 3 ]

```