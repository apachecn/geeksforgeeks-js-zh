# 洛达什 _。拆分()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-split-method/](https://www.geeksforgeeks.org/lodash-_-split-method/)

**洛达什 _。split()方法**按照给定的分隔符对给定的字符串进行拆分，最多可达给定的限制长度。

**语法:**

```
_.split( string, separator, limit )

```

**参数:** 此方法接受三个参数，如上所述，如下所述:

*   **String:** The string to be split.
*   **Separator:** Separator used to split strings.
*   **Limit:** The length of the result to be truncated.

**返回值:**这个方法返回一个数组。

**例 1:**

## Javascript

```
// Defining Lodash variable 
const _ = require('lodash'); 

var str = "Geeks-for-Geeks";

// Using _.replace() method
console.log(_.split(str, '-' ))
```

**输出:**

```
[ 'Geeks', 'for', 'Geeks' ]

```

**例 2:** 数组大小限制为 1。

## Javascript

```
// Defining Lodash variable 
const _ = require('lodash'); 

var str = "Geeks-for-Geeks";

// Using _.replace() method
console.log(_.split(str, '-', 1 ))
```

**输出:**

```
[ 'Geeks' ]

```

**注意:** 这在正常的 JavaScript 中不会起作用，因为它需要安装 lodash 库，可以使用 **npm 安装 lodash** 进行安装。