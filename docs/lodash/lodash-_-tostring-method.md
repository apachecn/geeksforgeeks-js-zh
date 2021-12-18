# 洛达什 _。toString()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-tostring-method/](https://www.geeksforgeeks.org/lodash-_-tostring-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、字符串、对象、数字等。

**_。toString()** 方法用于将给定值转换为字符串。对于空值和未定义的值，将返回空字符串。保留值-0 的符号。

**语法:**

```
_.toString( value )
```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **值:**此参数保存要转换的值。

**返回值:**这个方法返回转换后的字符串。

**例 1:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.toString() method 
console.log(_.toString(-0)); 
console.log(_.toString(['html', 'css', 'javascript']));
```

**输出:**

```
'-0'
'html,css,javascript'

```

**例 2:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.toString() method

// Will print an empty string
console.log(_.toString(null)); 
console.log(_.toString([1, 2, 3]));
```

**输出:**

```
''
'1,2,3'

```