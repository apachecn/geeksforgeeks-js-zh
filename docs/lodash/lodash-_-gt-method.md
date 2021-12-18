# 洛达什 _。gt()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-gt-method/](https://www.geeksforgeeks.org/lodash-_-gt-method/)

**_。gt()** **法**是用来求数值是否大于其他。如果该值大于另一个值，则返回 true。否则，它返回 false。

**语法:**

```
_.gt(value, other)

```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **Value:** This parameter holds the value to be compared.
*   **Other:** This parameter stores other values to be compared.

**返回值:**如果值大于另一个值，则该方法返回真，否则返回假。

**例 1:**

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.gt method 
console.log(_.gt(19, 8)); 
console.log(_.gt(15, 17)); 
```

**输出:**

```
true
false

```

**例二:**

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.gt method 
console.log(_.gt(13, 13)); 
console.log(_.gt(29, 17)); 
```

**输出:**

```
false
true

```