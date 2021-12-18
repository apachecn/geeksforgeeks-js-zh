# 洛达什 _。夹具()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-clamp-method/](https://www.geeksforgeeks.org/lodash-_-clamp-method/)

**_。夹钳()** **方法**用于夹钳上下界范围内的数字。

**语法:**

```
_.clamp(number, lower, upper)

```

**参数:**该方法接受三个参数，如上所述，如下所述:

*   **Number:** This parameter stores the number to be clamped.
*   **Lower limit:** This parameter keeps the lower limit.
*   **Upper limit:** This parameter keeps the upper limit.

**返回值:**此方法返回钳制数。

**例 1:**

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.clamp method 
console.log(_.clamp(2, 3, 5)); 
console.log(_.clamp(2, -2, -5)); 
```

**输出:**

```
3
-2

```

**例二:**

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.clamp method 
console.log(_.clamp(15, -13, 13)); 
console.log(_.clamp(-15, -13, 13)); 
```

**输出:**

```
13
-13

```