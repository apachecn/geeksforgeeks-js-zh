# 洛达什 _。isNaN()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-isnan-method/](https://www.geeksforgeeks.org/lodash-_-isnan-method/)

洛达什 **_。isNaN()方法**检查给定值是否为 NaN。这个方法和[的](https://www.geeksforgeeks.org/number-isnan-javascript/) [JavaScript isNaN()方法](https://www.geeksforgeeks.org/number-isnan-javascript/) 不一样，后者对于未定义的等非数值返回真。

**语法:**

```
_.isNaN( value )

```

**参数:** 该方法接受如上所述的单个参数，描述如下:

*   **值:**该参数保存需要检查 NaN 的值。

**返回值:**该方法返回一个**布尔值**(如果值为 NaN，则返回真，否则返回假)。

**例 1:**

## java 描述语言

```
// Defining Lodash variable 
const _ = require('lodash'); 

// Checking
console.log(_.isNaN(NaN));
```

**输出:**

```
true

```

**示例 2:** 对于使用空源进行检查，该方法返回 true。

## java 描述语言

```
// Defining Lodash variable 
const _ = require('lodash'); 

// Checking
console.log(_.isNaN(new Number(NaN)));
```

**输出:**

```
true

```

**例 3:** 这个方法也适用于数组。

## java 描述语言

```
// Defining Lodash variable 
const _ = require('lodash'); 

// Checking
console.log(_.isNaN(undefined)); 

// Checking
console.log(_.isNaN(10));
```

**输出:**

```
false
false

```