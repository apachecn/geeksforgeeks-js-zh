# 洛达什 _。isFinite()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-isfinite-method/](https://www.geeksforgeeks.org/lodash-_-isfinite-method/)

洛达什 **_。isFinite()方法**检查给定值是否为基元有限数，并返回相应的布尔值。

**语法:**

```
_.isFinite( value )

```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **值:**该参数保存要检查的原始有限数的值。

**返回值:**该方法返回一个**布尔值**(如果给定值是有限的，则返回真，否则返回假)。

**例 1:**

## java 描述语言

```
// Defining Lodash variable 
const _ = require('lodash'); 

// Checking for Finite Value 
console.log("The Value is Finite : "
        +_.isFinite(10));
```

**输出:**

```
The Value is Finite : true

```

**例 2:** 对于无穷大，返回 false。

## java 描述语言

```
// Defining Lodash variable 
const _ = require('lodash'); 

// Checking for Finite Value 
console.log("The Value is Finite : "
        +_.isFinite(Infinity));
```

**输出:**

```
The Value is Finite : false

```

**例 3:** 对于字符串，返回 false。

## java 描述语言

```
// Defining Lodash variable 
const _ = require('lodash'); 

// Checking for Finite Value 
console.log("The Value is Finite : "
        + _.isFinite("gfg"));
```

**输出:**

```
The Value is Finite : false

```

**例 4:**

## java 描述语言

```
// Defining Lodash variable 
const _ = require('lodash'); 

// Checking for Finite Value 
console.log("The Value is Finite : "
    +_.isFinite(Number.MAX_VALUE));
```

**输出:**

```
The Value is Finite : true

```