# 洛达什 _。startCase()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-startcase-method/](https://www.geeksforgeeks.org/lodash-_-startcase-method/)

**_。startCase()** **方法**用于转换字符串以启动案例。

**语法:**

```
_.startCase( [string=''] )

```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **String:** This parameter holds the string to be converted.

**返回值:**此方法返回事例字符串的开始。

下面的例子说明了 Lodash _。JavaScript 中的 startCase()方法:

**例 1:**

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.startCase() method 
console.log(_.startCase('geeks for geeks')); 
console.log(_.startCase('geeksforgeeks'));
console.log(_.startCase('@#$%geeksforgeeks@#$%'));
```

**输出:**

```
'Geeks For Geeks'
'Geeksforgeeks'
'Geeksforgeeks'

```

**例二:**

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.startCase() method 
console.log(_.startCase(null)); 
console.log(_.startCase('123456789'));
console.log(_.startCase("gfg.Id"));
```

**输出:**

```
''
'123456789'
'Gfg Id'

```