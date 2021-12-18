# 下划线. js _。不是()方法

> 原文:[https://www.geeksforgeeks.org/underscore-js-_-not-method/](https://www.geeksforgeeks.org/underscore-js-_-not-method/)

_。**而不是**()方法 r 返回一个布尔值，该值与给定值的真布尔值相反。

**语法:**

```
_.not( value );

```

**参数:**

*   **值:**返回相反布尔值的给定值。

**返回值:**该方法返回一个**布尔值。**

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。可以使用 **npm 安装下划线-contrib-save 来安装下划线. js contrib 库。**

**例 1:** 该方法返回 false。

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var bool = _.not( true );

console.log("Opposite boolean value if"
    + " value's truthiness is : ", bool);
```

**输出:**

```
Opposite boolean value if value's truthiness is :  false

```

**例 2:** 为假，则该方法返回与真相反的值。

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var bool = _.not( false );

console.log("Opposite boolean value if"
    + " value's truthiness is : ", bool);
```

**输出:**

```
Opposite boolean value if value's truthiness is :  true

```

**示例 3:** 对于现有值，此方法返回 false。

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var bool = _.not( "Geeks" );

console.log("Opposite boolean value if"
    + " value's truthiness is : ",bool);
```

**输出:**

```
Opposite boolean value if value's truthiness is :  false

```

**示例 4:** 对于不存在的值，此方法返回 true。

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var bool = _.not( null );

console.log("Opposite boolean value if"
    + " value's truthiness is : ", bool);
```

**输出:**

```
Opposite boolean value if value's truthiness is :  true

```