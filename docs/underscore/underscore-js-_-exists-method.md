# 下划线. js _。存在()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-exists-method/](https://www.geeksforgeeks.org/underscore-js-_-exists-method/)

_。**存在**()方法检查给定值是否为“Existy”，对应返回一个布尔值。空值和未定义的都被认为是不存在的值。所有其他值都是“Existy”。

**语法:**

```
_.exists( value );

```

**参数:**

*   **值:**要检查存在值的给定值。

**返回值:**该方法返回一个**布尔值**(如果给定值为 Existy，则返回 true，否则返回 false)。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。

可以使用 **npm 安装下划线-contrib–save 来安装下划线. js contrib 库。**

**例 1:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var bool = _.exists("Geeks");;

console.log("Given Value is Existy : ",bool);
```

**输出:**

```
Given Value is Existy : true
```

**例 2:** 对于未定义，返回 false。

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var bool = _.exists(undefined);;

console.log("Given Value is Existy : ",bool);
```

**输出:**

```
Given Value is Existy : false
```

**例 3:** 同样为空，返回 false。

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var bool = _.exists(null);;

console.log("Given Value is Existy : ", bool);
```

**输出:**

```
Given Value is Existy : false
```

**例 4:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var bool = _.exists([1,12,2,3]);;

console.log("Given Value is Existy : ", bool);
```

**输出:**

```
Given Value is Existy : true
```