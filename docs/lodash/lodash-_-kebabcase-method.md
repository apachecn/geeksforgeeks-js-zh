# 洛达什 _。kebabCase()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-kebabcase-method/](https://www.geeksforgeeks.org/lodash-_-kebabcase-method/)

Lodash 是一个工作在下划线. js 之上的 JavaScript 库，Lodash 有助于处理数组、集合、字符串、对象、数字等。

_。kebab case()方法用于将给定字符串转换为 kebab 大小写字符串。[kebbbase](https://en.wikipedia.org/wiki/Letter_case#Special_case_styles)是用连字符代替空格书写标识符的做法。

**语法:**

```
_.kebabCase([string=''])

```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **字符串:**此参数保存需要转换为烤串大小写字符串的字符串。

**返回值:**该方法返回串包串。

**例 1:**

## Javascript

```
const _ = require('lodash'); 

var str1 = _.kebabCase("GEEKS FOR GEEKS");
console.log(str1);

var str2 = _.kebabCase("GFG--Geeks");
console.log(str2);
```

**输出:**

```
"geeks-for-geeks"
"gfg-geeks"

```

**例二:**

## Javascript

```
const _ = require('lodash'); 

var str1 = _.kebabCase("GEEKS__FOR__GEEKS");
console.log(str1);

var str2 = _.kebabCase("GEEKS-----FOR_____Geeks");
console.log(str2);

var str3 = _.kebabCase("geeks--FOR--geeks");
console.log(str3);
```

**输出:**

```
"geeks-for-geeks"
"geeks-for-geeks"
"geeks-for-geeks"

```