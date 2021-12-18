# 下划线. js _。eq()方法

> 原文:[https://www.geeksforgeeks.org/underscore-js-_-eq-method/](https://www.geeksforgeeks.org/underscore-js-_-eq-method/)

_。 **eq()** 方法 c 用松散的等式( == )来补充论点。

```
_.eq( val1, val2,..., valn );

```

**参数:**该方法取 n 个值对其进行运算。

**返回值:**这个方法 r 返回一个布尔值( **true** 如果参数相等则返回 **false** )。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。

可以使用 **npm 安装下划线-contrib–save 来安装下划线. js contrib 库。**

**例 1:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var equal  = _.eq( 1, "1" );

console.log("The Given values are equal :",equal);
```

**输出:**

```
The Given values are equal : true

```

**例 2:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var equal  = _.eq( "Geeks", "Geeks" );

console.log("The Given values are equal :",equal);
```

**输出:**

```
The Given values are equal : true

```

**示例 3:** 有效值返回真，因此与真布尔值比较时，比较返回真。

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var equal  = _.eq( 1, true );

console.log("The Given values are equal :",equal);
```

**输出:**

```
The Given values are equal : true

```

**示例 4:** 有效值返回真，因此与假布尔值进行比较时，比较返回假。

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var equal  = _.eq( 1, false );

console.log("The Given values are equal :",equal);
```

**输出:**

```
The Given values are equal : false

```