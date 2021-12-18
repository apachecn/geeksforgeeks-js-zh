# 洛达什 _。trimStart()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-trimstart-method/](https://www.geeksforgeeks.org/lodash-_-trimstart-method/)

洛达什 **_。trimStart()方法** r 从给定的字符串中删除前导空格或指定字符。

**语法:**

```
_.trimStart( string, chars )

```

**参数:** 此方法接受两个参数，如上所述，如下所述:

*   **String:** This parameter stores the string to be trimmed.
*   **Character:** This parameter stores the character set to be specially trimmed.

**返回值:**这个方法返回一个修剪后的字符串。

**例 1:**

## Javascript

```
// Defining Lodash variable
const _ = require('lodash');

var str = "   Geeks-for-Geeks   ";

// Using _.trimStart() method
console.log(_.trimStart(str));
```

**输出:**

```
"Geeks-for-Geeks   "

```

**示例 2:** 从字符串中显式修剪“-”。

## Javascript

```
// Defining Lodash variable
const _ = require('lodash');

var str = "----GeeksforGeeks----";

// Using _.trimStart() method
console.log(_.trimStart(str, "-"))
```

**输出:**

```
"GeeksforGeeks----"

```

**注意:** 这在正常的 JavaScript 中不会起作用，因为它需要安装 lodash 库，可以使用 npm 安装 lodash 进行安装。