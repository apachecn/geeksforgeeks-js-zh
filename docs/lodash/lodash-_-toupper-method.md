# 洛达什 _。toUpper()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-toupper-method/](https://www.geeksforgeeks.org/lodash-_-toupper-method/)

Lodash 是一个工作在下划线. js 之上的 JavaScript 库，Lodash 有助于处理数组、字符串、对象、数字等。

**_。toUpper()** **方法**用于将整个字符串转换为大写。此方法不影响任何大写的特殊字符、数字和字母。

**语法:**

```
_.toUpper( [string = ''])

```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **字符串:**此参数保存要转换的字符串。

**返回值:**该方法返回大写字符串。

**例 1:**

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.toUpper() method 
console.log(_.toUpper('Geeks-For-Geeks')); 
console.log(_.toUpper('#--GeeksForGeeks--#')); 
```

**输出:**

```
'GEEKS-FOR-GEEKS'
'#--GEEKSFORGEEKS--#'

```

**例二:**

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");  

//  Given string     
let str = "Hello Geeks!";

// Use of _.toUpper() method 
console.log(_.toUpper(str)); 
```

**输出:**

```
'HELLO GEEKS!'

```