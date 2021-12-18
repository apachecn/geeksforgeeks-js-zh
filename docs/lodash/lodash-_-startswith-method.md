# 洛达什 _。用()方法启动

> 原文:[https://www.geeksforgeeks.org/lodash-_-startswith-method/](https://www.geeksforgeeks.org/lodash-_-startswith-method/)

**_。startsWith()** **方法**用于查找字符串是否以给定的目标字符串开始。如果字符串以给定的目标字符串开头，则返回 true。否则，它返回 false。

**语法:**

```
_.startsWith( [string = ''], [target], [position = 0] )

```

**参数:**该方法接受三个参数，如上所述，如下所述:

*   **String:** This parameter stores the string to be checked.
*   **Target:** This parameter stores the string to be searched.
*   **Location:** This parameter stores the location to be searched.

**返回值:**如果字符串以目标字符串开头，则该方法返回 true，否则返回 false。

以下示例说明了 Lodash _。JavaScript 中的 startsWith()方法:

**例 1:**

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.startsWith() method 
console.log(_.startsWith('geeksforgeeks', 'g')); 
console.log(_.startsWith('geeksforgeeks', 'f'));
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

// Use of _.startsWith() method 
console.log(_.startsWith('geeksforgeeks', 'e', 1 )); 
console.log(_.startsWith('geeksforgeeks', 'e', 4 )); 
console.log(_.startsWith('geeksforgeeks', 'e', 10));
```

**输出:**

```
true
false
true

```