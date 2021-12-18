# 洛达什 _。defaultTo()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-defaultto-method/](https://www.geeksforgeeks.org/lodash-_-defaultto-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、字符串、对象、数字等。

**_。defaultTo()** **方法**用于检查给定的*值*，并确定是否应该恢复默认值。当值为 NaN、null 或未定义时，返回*默认值*参数中给出的值。

**语法:**

```
_.defaultTo( value, defaultValue )

```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **值:**该参数保存要检查的值。
*   **默认值:**此参数保存要恢复的默认值。

**返回值:**该方法返回解析值。

**例 1:**

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");  

// Return the resolved value 
// by _.defaultTo() method
console.log(_.defaultTo(5, 15));

// Return the resolved value
// by _.defaultTo() method
console.log(_.defaultTo(82, 43));
```

**输出:**

```
5
82

```

**例二:**

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");  

// When the value is NaN, defaultValue 
// is returned by _.defaultTo() method
console.log(_.defaultTo(null, 15));

// When the value is undefined, defaultValue 
// is returned by _.defaultTo() method
console.log(_.defaultTo(undefined, 43));
```

**输出:**

```
15
43
```