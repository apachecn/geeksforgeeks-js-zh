# 洛达什 _。重复()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-repeat-method/](https://www.geeksforgeeks.org/lodash-_-repeat-method/)

Lodash 是一个工作在下划线. js 之上的 JavaScript 库，Lodash 有助于处理数组、字符串、对象、数字等。

**_。重复()** **方法**用于重复给定的字符串 n 次。

**语法:**

```
_.repeat(string, n)
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **字符串:**此参数保存要重复的字符串。
*   **n:** n 是重复字符串的次数。

**返回值:**这个方法返回重复的字符串。

**例 1:**

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.repeat() method 
console.log(_.repeat('#', 4)); 
console.log(_.repeat('gfg', 3));
```

**输出:**

```
####
gfggfggfg

```

**例二:**

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.repeat() method 
console.log(_.repeat('GeeksforGeeks', 0)); 
console.log(_.repeat('_GFG_', 3));
```

**输出:**

```
''
_GFG__GFG__GFG_

```