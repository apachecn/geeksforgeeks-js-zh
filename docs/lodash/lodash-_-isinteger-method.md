# 洛达什 _。isInteger()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-isinteger-method/](https://www.geeksforgeeks.org/lodash-_-isinteger-method/)

洛达什 **_。方法**检查给定值是否为整数，并返回相应的布尔值。

**语法:**

```
_.isInteger( value )

```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **值:**该参数保存需要检查整数的值。

**返回值:**该方法返回一个**布尔值**(如果给定值是整数，则返回真，否则返回假)。

**例 1:**

## java 描述语言

```
// Defining Lodash variable 
const _ = require('lodash'); 

// Checking for Integer
console.log("The Value is Integer : "
        + _.isInteger(100));
```

**输出:**

```
The Value is Integer : true

```

**示例 2:** 对于包含整数的字符串，此方法返回 false。

## java 描述语言

```
// Defining Lodash variable 
const _ = require('lodash'); 

// Checking for Integer
console.log("The Value is Integer : "
        + _.isInteger("10"));
```

**输出:**

```
The Value is Integer : false

```

**例 3:** 对于 Infinity 值，返回 false。

## java 描述语言

```
// Defining Lodash variable 
const _ = require('lodash'); 

// Checking for Integer
console.log("The Value is Integer : "
        + _.isInteger(Infinity));
```

**输出:**

```
The Value is Integer : false

```