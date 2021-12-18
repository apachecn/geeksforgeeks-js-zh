# 洛达什 _。字数()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-words-method/](https://www.geeksforgeeks.org/lodash-_-words-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、字符串、对象、数字等。

**_。words()方法**用于将给定的  字符串拆分成一个单词数组。可以指定一个模式，以便从字符串中删除某些单词。

**语法:**

```
_.words( string, pattern )

```

**参数:** 该方法接受两个参数，如上所述，描述如下:

*   **字符串:**是要拆分的字符串。默认值为空字符串。
*   **模式:**这是一个单词匹配的模式。这是一个可选参数。

**返回值:**这个方法根据模式返回一个单词数组。

**例 1:**

## java 描述语言

```
// Defining Lodash variable 
const _ = require('lodash'); 

// Specify the string to split
var str = "Geeks for Geeks";

// Using _.words() method
console.log(_.words(str));
```

**输出:**

```
[ 'Geeks', 'for', 'Geeks' ]

```

**例 2:**

## java 描述语言

```
// Defining Lodash variable 
const _ = require('lodash'); 

// Specify the string to split
var str = "Geeks for Geeks";

// Using _.words() method
console.log(_.words(str, "for"));
```

**输出:**

```
[ 'for', index: 6, input: 'Geeks for Geeks', groups: undefined ]

```

**例 3:**

## java 描述语言

```
// Defining Lodash variable 
const _ = require('lodash'); 

// Specify the string to split
var str = "& Geeks for Geeks &";

// Using _.words() method with
// a given pattern
console.log(_.words(str, /[^, ]+/g));
```

**输出:**

```
[ '&', 'Geeks', 'for', 'Geeks', '&' ]

```