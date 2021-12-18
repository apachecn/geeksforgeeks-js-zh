# 洛达什 _。isArrayLike()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-isarraylike-method/](https://www.geeksforgeeks.org/lodash-_-isarraylike-method/)

洛达什 **_。isArrayLike()方法**检查该值是否像数组一样。如果一个值不是一个函数并且有一个值，那么它就被认为是类似数组的。长度是大于或等于 0 且小于或等于数字的整数。MAX_SAFE_INTEGER。

**语法:**

```
_.isArrayLike(value)
```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **Value:** This parameter stores the values of similar array values that need to be checked.

**返回值:**该方法返回一个**布尔值**。

**例 1:** 此方法返回数组的**真**。

## Javascript

```
// Defining Lodash variable
const _ = require('lodash'); 

var val = [1, 2, 3]

// Checking for an ArrayLike
console.log("The Value is ArrayLike : " 
    +_.isArrayLike(val));
```

**输出:**

```
The Value is ArrayLike : true
```

**示例 2:** 该方法返回字符串的 **true** ，因为可以计算它们的长度。

## Javascript

```
// Defining Lodash variable
const _ = require('lodash'); 

var val = "GeeksforGeeks";
// Checking for an ArrayLike
console.log("The Value is ArrayLike : "
    +_.isArrayLike(val)); 
```

**输出:**

```
The Value is ArrayLike : true

```

**例 3:** 当此方法返回**为假时**。

## Javascript

```
// Defining Lodash variable
const _ = require('lodash'); 

var val = { 1:1 };
// Checking for an ArrayLike
console.log("The Value is ArrayLike : " 
    +_.isArrayLike(val)); 
```

**输出:**

```
The Value is ArrayLike : false

```

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装 lodash 库，可以使用 **npm install lodash** 进行安装。