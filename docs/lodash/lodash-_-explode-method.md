# 洛达什 _。爆炸()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-explode-method/](https://www.geeksforgeeks.org/lodash-_-explode-method/)

**洛达什 _。explot()方法**用于将一个字符串分解成一个字符数组。

**语法:**

```
_.explode( String );

```

**参数:**此法取单参数如上所述，描述如下:

*   **String:** This method takes a string to explode.

**返回值:**该方法返回生成的字符数组。

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装 lodash.js contrib 库。可以使用 **npm 安装 Lodash.js contrib 库-保存**。

**例 1:**

## Javascript

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

var a  = _.explode( "GeeksforGeeks" ); 

console.log("The generated array is : ", a);
```

**输出:**

```
The generated array is :
["G", "e", "e", "k", "s", "f", "o", "r", "G", "e", "e", "k", "s"]

```

**例二:**

## Javascript

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

var a  = _.explode( "Computer Science Portal" ); 

console.log("The generated array is : ", a);
```

**输出:**

```
The generated array is : [
    "C", "o", "m", "p", "u", "t", "e", "r", 
    " ", "S", "c", "i", "e", "n", "c", "e", 
    " ", "P", "o", "r", "t", "a", "l"
]

```