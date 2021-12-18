# 洛达什 _。parseInt()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-parseint-method/](https://www.geeksforgeeks.org/lodash-_-parseint-method/)

**_。parseInt()** **方法**用于解析字符串参数，并返回指定基数的整数。

**语法:**

```
_.parseInt( string, [radix = 10] )

```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **String:** This parameter holds the string to be converted.
*   **Cardinality:** This parameter stores the cardinality of the interpretation value (the default value is 10).

**返回值:**该方法返回转换后的整数。

以下示例说明了 Lodash _。JavaScript 中的 parseInt()方法:

**例 1:**

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.parseInt() method 
console.log(_.parseInt("10.33")); 
console.log(_.parseInt("8", 8));
console.log(_.parseInt("100", 10));
```

**输出:**

```
10
NaN
100
```

**例二:**

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.parseInt() method 
console.log(_.parseInt("0x10")); 
console.log(_.parseInt("10 year of gfg"));
```

**输出:**

```
16
10

```