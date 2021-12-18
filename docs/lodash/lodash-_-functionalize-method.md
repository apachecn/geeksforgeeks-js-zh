# 洛达什 _。功能化()方法

> 原文:[https://www . geesforgeks . org/lo dash-_-functional-method/](https://www.geeksforgeeks.org/lodash-_-functionalize-method/)

洛达什 **_。functionalize()** 方法 t 取一个函数(使用 **这个** 的那个)并将 **这个** 推入参数列表。返回的函数使用其第一个参数作为原始函数的接收者/上下文，其余参数用作原始函数的整个参数列表。

**语法:**

```
_.functionalize( function )

```

**参数:**该方法接受如上所述的单个参数，定义如下:

*   **函数:**这个方法取一个使用**这个**的函数。

**返回值:**这个方法 r 返回一个函数。

**注意:**要执行以下示例，您必须使用此命令提示符安装 **lodash-contrib** 库，并执行以下命令。

```
npm install lodash-contrib

```

以下示例说明了 Lodash _。JavaScript 中 functionalize()方法:

**例 1:**

## java 描述语言

```
// Defining lodash contrib variable
var _ = require('lodash-contrib'); 

function get(g) {
        return this[g];
    }

var geekFunc = _.functionalize(geta);

var geeks = {
    GeeksforGeeks: "Computer Science Portal for Geeks"
};
console.log(geekFunc(geeks,"GeeksforGeeks"))
```

**输出:**

```
Computer Science Portal for Geeks

```

**例 2:**

## java 描述语言

```
// Defining lodash contrib variable
var _ = require('lodash-contrib'); 

function get(g) {
        return this[g];
    }

var geekFunc = _.functionalize(get);

var geeks = {
    GeeksforGeeks: 1000000
};
console.log(geekFunc(geeks,"GeeksforGeeks"))
```

**输出:**

```
1000000

```