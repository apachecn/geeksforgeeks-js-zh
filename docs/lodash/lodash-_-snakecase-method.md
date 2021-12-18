# 洛达什 _。蛇箱()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-snakecase-method/](https://www.geeksforgeeks.org/lodash-_-snakecase-method/)

**_。**蛇案()**方法**用于将字符串转换为蛇案。Snake case 是指将单词组合成小写字符串，单词之间用下划线(_)。

**语法:**

```
_.snakeCase( [string=''] )

```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **String:** This parameter holds the string to be converted.

**返回值:**这个方法返回蛇的大小写字符串。

下面的例子说明了 Lodash _。JavaScript 中的蛇案例()方法:

**例 1:**

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.snakeCase() method 
console.log(_.snakeCase('Geeks For Geeks')); 
console.log(_.snakeCase('GeeksForGeeks'));
console.log(_.snakeCase('@#$%GeeksForGeeks@#$%'));
```

**输出:**

```
'geeks_for_geeks'
'geeks_for_geeks'
'geeks_for_geeks'

```

**例二:**

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.snakeCase() method 
console.log(_.snakeCase(null)); 
console.log(_.snakeCase('123456789'));
console.log(_.snakeCase("gfg.Id"));
```

**输出:**

```
''
'123456789'
'gfg_id'

```