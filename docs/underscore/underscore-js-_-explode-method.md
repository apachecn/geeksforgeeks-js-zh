# 下划线. js _。爆炸()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-explode-method/](https://www.geeksforgeeks.org/underscore-js-_-explode-method/)

**_。explot()**方法用于将一个字符串扩展成一个字符数组。

**语法:**

```
_.explode( String );
```

**参数:**

*   **String:** This method takes string explosion.

**返回值:**这个方法 r 返回生成的字符数组。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。可以使用 **npm 安装下划线-contrib-save 来安装下划线. js contrib 库。**

**例 1:**

## Javascript

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var a  = _.explode( "GeeksforGeeks" );

console.log("The generated array is : ", a);
```

**输出:**

```
The generated array is :  [
  'G', 'e', 'e', 'k',
  's', 'f', 'o', 'r',
  'G', 'e', 'e', 'k',
  's'
]

```

**例二:**

## Javascript

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var a  = _.explode( "Computer Science Portal" );

console.log("The generated array is : ", a);
```

**输出:**

```
The generated array is :  [
  'C', 'o', 'm', 'p', 'u',
  't', 'e', 'r', ' ', 'S',
  'c', 'i', 'e', 'n', 'c',
  'e', ' ', 'P', 'o', 'r',
  't', 'a', 'l'
]

```