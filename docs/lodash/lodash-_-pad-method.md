# 洛达什 _。pad()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-pad-method/](https://www.geeksforgeeks.org/lodash-_-pad-method/)

_。pad()方法用于在字符串短于给定长度的情况下在左侧和右侧填充字符串。如果长度不能平均分配，则填充字符将被截断。

**语法:**

```
_.pad([string=''], [length=0], [chars=' '])

```

**参数:**该方法接受三个参数，如上所述，如下所述:

*   **String:** This parameter stores the string to be filled.
*   **Length:** This parameter stores the filling length.
*   **Character:** This parameter holds the string used as padding.

**返回值:**这个方法返回填充字符串。

**例 1:**

## Javascript

```
const _ = require('lodash'); 

var str1 = _.pad("GEEKS", 25, '-*-');
console.log(str1);

var str2 = _.pad("GFG--Geeks", 30, 'gfg');
console.log(str2);
```

**输出:**

```
"-*--*--*--GEEKS-*--*--*--"
"gfggfggfggGFG--Geeksgfggfggfgg"

```

**例二:**

## Javascript

```
const _ = require('lodash'); 

var str1 = _.pad("GEEKS__FOR__GEEKS", 20, '_');
console.log(str1);

var str2 = _.pad("G4G--geeks--GEEKS", 25, '*');
console.log(str2);

var str3 = _.pad("GEEKS-----FOR_____Geeks", 20);
console.log(str3);
```

**输出:**

```
"_GEEKS__FOR__GEEKS__"
"****G4G--geeks--GEEKS****"
"gEEKS-----FOR_____Geeks"

```