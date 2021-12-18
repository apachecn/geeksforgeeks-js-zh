# 洛达什 _。padStart()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-padstart-method/](https://www.geeksforgeeks.org/lodash-_-padstart-method/)

**_。padStart()** **法**是用一根弦垫另一根弦，直到达到给定的长度。填充从字符串的左端应用。如果填充字符超过长度，将被截断。

**语法:**

```
_.padStart( [string = ''], [length = 0], [chars = ' '] )
```

**参数:**该方法接受三个参数，如上所述，如下所述:

*   **String:** This parameter saves the string to pad.
*   **Length:** This parameter stores the length of the pad.
*   **Character:** This parameter holds the string used as padding.

**返回值:**这个方法返回填充字符串。

以下示例说明了 Lodash _。JavaScript 中的 padStart()方法:

**例 1:**

## Javascript

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Use of _.padStart method
console.log(_.padStart('GFG', 5));
console.log(_.padStart('1234', 6, '#'));
```

**输出:**

```
'  GFG'
'##1234'
```

**例二:**

## Javascript

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Use of _.padStart method
console.log(_.padStart('GFG', 6, '-'));
console.log(_.padStart('1234', 3, '#'));
```

**输出:**

```
'---GFG'
'1234'
```