# 洛达什 _。isLength()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-islength-method/](https://www.geeksforgeeks.org/lodash-_-islength-method/)

洛达什 **_。isLength()方法**检查给定值是否为类似数组的长度，并返回相应的布尔值。

**语法:**

```
_.isLength( value )

```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **值:**此参数保存需要检查类似数组长度的值。

**返回值:**该方法返回一个**布尔值**(如果给定值是一个类似数组的长度，则返回真，否则返回假)。

**例 1:**

## java 描述语言

```
// Defining Lodash variable 
const _ = require('lodash'); 

// Checking for Length
console.log("The Value is Length : "
        + _.isLength(100));
```

**输出:**

```
The Value is Length : true

```

**例 2:** 对于无穷大，返回 false。

## java 描述语言

```
// Defining Lodash variable 
const _ = require('lodash'); 

// Checking for Length 
console.log("The Value is Length : "
        + _.isLength(Infinity));
```

**输出:**

```
The Value is Length : false

```

**例 3:** 对于字符串，返回 false。

## java 描述语言

```
// Defining Lodash variable 
const _ = require('lodash'); 

// Checking for Length 
console.log("The Value is Length : "
        + _.isLength("len"));
```

**输出:**

```
The Value is Length : false

```

**例 4:**

## java 描述语言

```
// Defining Lodash variable 
const _ = require('lodash'); 

// Checking for Length 
console.log("The Value is Length : "
        + _.isLength(Number.MAX_VALUE));
```

**输出:**

```
The Value is Length : true

```