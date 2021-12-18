# 洛达什 _。isMatchWith()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-ismatchwith-method/](https://www.geeksforgeeks.org/lodash-_-ismatchwith-method/)

洛达什 **_。isMatchWith()方法** p 对对象和源进行部分深度比较，以确定对象是否包含等效属性值。由于 p 人工比较，它将空数组和空对象源值分别与任何数组或对象值进行匹配。该方法接受另一个函数作为“定制器”，调用该函数来比较值。

**语法:**

```
_.isMatchWith( object, source, [customizer] )

```

**参数:** 该方法接受三个参数，如上所述，描述如下:

*   **对象:**要匹配来源的对象。
*   **来源:**要匹配的来源。
*   **定制器:**用于定制比较的功能。

**返回值:**该方法返回一个**布尔值。**如果源和给定对象匹配，则返回真，否则返回假。

**例 1:**

## java 描述语言

```

// Defining Lodash variable 
const _ = require('lodash'); 

var object = { 'Geeks': "GfG", 'Geeks2': "GfG2" };

function fun() {
    return true;
}

// Checking
console.log(_.isMatch(object, { 'Geeks2': "GfG2" }, fun)); 

// Checking
console.log(_.isMatch(object, { 'Geeks': "GfG2" }, fun)); 
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

function fun(){
    return true;
}

// Checking
console.log(_.isMatch(object, { }, fun)); 
```

**输出:**

```
true
```