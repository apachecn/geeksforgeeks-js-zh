# 洛达什 _。擒纵表达式()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-escaperegexp-method/](https://www.geeksforgeeks.org/lodash-_-escaperegexp-method/)

_。方法用于转义正则表达式中的特殊字符“^”、“内容”。, "", ".", "*", "+", "?字符串中的“、”(“”、“”、“[”、“]”、“{”、“}”和“|”。

**语法:**

```
_.escapeRegExp([string=''])

```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **String:** This parameter holds the string to be escaped.

**返回值:**此方法返回转义字符串。

**例 1:**

## Javascript

```
const _ = require('lodash'); 

var str1 = _.escapeRegExp("/a/");
console.log(str1);

var str2 = _.escapeRegExp("\*?{}.");
console.log(str2);
```

**输出:**

```
"/a/"
"\\*\\?\\{\\}\\."

```

**例二:**

## Javascript

```
const _ = require('lodash'); 

var str1 = _.escapeRegExp("/geeks/");
console.log(str1);

var str2 = _.escapeRegExp("/(?<geeks>.)(?<for>.)(?<geeks>.)/");
console.log(str2);

var str3 = _.escapeRegExp("\*?????{}.");
console.log(str3);
```

**输出:**

```
"/geeks/"
"/\\(\\?<geeks>\\.\\)\\(\\?<for>\\.\\)\\(\\?<geeks>\\.\\)/"
"\\*\\?\\?\\?\\?\\?\\{\\}\\."

```