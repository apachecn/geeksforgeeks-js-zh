# 洛达什 _。去毛刺()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-deburr-method/](https://www.geeksforgeeks.org/lodash-_-deburr-method/)

Lodash 是一个工作在下划线. js 之上的 JavaScript 库，Lodash 有助于处理数组、字符串、对象、数字等。

_。deburr()方法用于将 Latin-1 Supplement 和 Latin Extended-A 字母转换为基本拉丁字母，并移除组合变音符号。

**语法:**

```
_.deburr([string=''])
```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **字符串:**此参数保存拉丁-1 增补和拉丁扩展-A 字母字符串。

**返回值:**此方法返回基本拉丁字母字符串。

**例 1:**

## Javascript

```
const _ = require('lodash'); 

var str1 = _.deburr("ÀÄÅÆÇÈÉ");
console.log(str1);

var str2 = _.deburr("ãäåæçè");
console.log(str2);
```

**输出:**

```
"AAAAeCEE"
"aaaaece"

```

**例二:**

## Javascript

```
const _ = require('lodash'); 

var str1 = _.deburr("ĜĚĔĶŜ");
console.log(str1);

var str2 = _.deburr("ĝęėķś");
console.log(str2);
```

**输出:**

```
"GEEKS"
"geeks"

```