# 下划线. js _。快照()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-快照-方法/](https://www.geeksforgeeks.org/underscore-js-_-snapshot-method/)

**_。snapshot()方法**用于对给定对象进行深度快照或克隆。

**语法:**

```
_.snapshot( obj );

```

**参数:**该方法取一个对象创建一个深度克隆。

**返回值:**这个方法返回一个克隆对象。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。

可以使用 **npm 安装下划线-contrib-save 来安装下划线. js contrib 库。**

**例 1:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 
var given_Object = { 1:"a", 2:"b" };
var obj = _.snapshot(given_Object);;

console.log("Cloned Object: ", obj);
```

**输出:**

```
Cloned Object:  { '1': 'a', '2': 'b' }

```

**示例 2:** 该方法对于数组也很有效。

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 
var given_Object = [ 1, 2 ,3 ,4 ];
var obj = _.snapshot(given_Object);;

console.log("Cloned Object: ", obj);
```

**输出:**

```
Cloned Object:  [ 1, 2, 3, 4 ]

```

**例 3:** 这个方法也适用于字符串。

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 
var given_Object = "GeeksforGeeks"
var obj = _.snapshot(given_Object);;

console.log("Cloned Object: ", obj);
```

**输出:**

```
Cloned Object:  GeeksforGeeks

```

**例 4:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 
var given_Object = 10000;
var obj = _.snapshot(given_Object);;

console.log("Cloned Object: ", obj);
```

**输出:**

```
Cloned Object:  10000

```