# 下划线. js _。内爆()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-内爆-方法/](https://www.geeksforgeeks.org/underscore-js-_-implode-method/)

**_。内爆()**方法用于将一组字符串内爆为单个字符串。

**语法:**

```
_.implode( array );
```

**参数:**

*   **数组:**这个方法需要一个数组才能内爆。

**返回值:**这个方法返回生成的字符串。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。

可以使用 **npm 安装下划线-contrib–save 来安装下划线. js contrib 库。**

**例 1:**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var s  = _.implode( ["G", "e", "e", "k",
                     "s", "f", "o", "r",
                     "G", "e", "e", "k", "s"] );

console.log("The generated String is : ", s);
```

**输出:**

```
The generated String is :  GeeksforGeeks
```

**例 2:**

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var s  = _.implode( ["C", "o", "m", "p", "u", "t",
                     "e", "r", " ", "S", "c", "i",
                     "e", "n", "c", "e", " ", "P",
                     "o", "r", "t", "a", "l"] );

console.log("The generated String is : ", s);
```

**输出:**

```
The generated String is :  Computer Science Portal
```