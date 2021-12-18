# 洛达什 _。isMatch()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-ismatch-method/](https://www.geeksforgeeks.org/lodash-_-ismatch-method/)

洛达什 **_。isMatch()方法** p 对对象和源进行部分深度比较，以确定对象是否包含等效属性值。由于 p 人工比较，它将空数组和空对象源值分别与任何数组或对象值进行匹配。

**语法:**

```
_.isMatch( object, source )

```

**参数:** 该方法接受两个参数，如上所述，描述如下:

*   **对象:**要匹配来源的对象。
*   **来源:**要匹配的来源。

**返回值:**该方法返回一个**布尔值**(如果源和给定对象匹配，则返回真，否则返回假)。

**例 1:**

## java 描述语言

```
// Defining Lodash variable 
const _ = require('lodash'); 

var object = { 'Geeks': "GfG", 'Geeks2': "GfG2" };

// Checking
console.log(_.isMatch(object, { 'Geeks2': "GfG2" })); 

// Checking
console.log(_.isMatch(object, { 'Geeks': "GfG2" }));
```

**输出:**

```
true
false

```

**示例 2:** 对于使用空源进行检查，该方法返回 true。

## java 描述语言

```
// Defining Lodash variable 
const _ = require('lodash'); 

var object = { 'Geeks': "GfG", 'Geeks2': "GfG2" };

// Checking
console.log(_.isMatch(object, { }));
```

**输出:**

```
true

```

**例 3:** 这个方法也适用于数组。

## java 描述语言

```
// Defining Lodash variable 
const _ = require('lodash'); 

var object = [1, 2, 3];

// Checking
console.log(_.isMatch(object, [1, 2])); 

// Checking
console.log(_.isMatch(object, [1, 3]));
```

**输出:**

```
true
false

```