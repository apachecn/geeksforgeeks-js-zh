# 洛达什 _。eq()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-eq-method/](https://www.geeksforgeeks.org/lodash-_-eq-method/)

**_。eq()** **方法**用于通过执行 SameValueZero 比较来查找两个值是否相等。如果值相等，则返回 true。否则，它返回 false。

**语法:**

```
_.eq(value, other)

```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **Value:** This parameter holds the value to be compared.
*   **Other:** This parameter stores other values to be compared.

**返回值:**如果值相等，该方法返回真，否则返回假。

**例 1:**

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.eq method 
console.log(_.eq("Geeks", "Geeks" )); 
console.log(_.eq("Geeks", Object("Geeks"))); 
console.log(_.eq(NaN, NaN)); 
```

**输出:**

```
true
false
true

```

**例二:**

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");  

// Given values
var object = { 'gfg': 2020 };
var other = { 'gfg': 2020 };

// Use of _.eq method 
console.log(_.eq(object, object)); 
console.log(_.eq(object, other)); 
```

**输出:**

```
true
false

```