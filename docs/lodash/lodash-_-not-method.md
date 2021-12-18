# 洛达什 _。不是()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-not-method/](https://www.geeksforgeeks.org/lodash-_-not-method/)

**洛达什 _。not()方法**返回一个与给定值的真布尔值相反的布尔值。

**语法:**

```
_.not( value );
```

**参数:**该方法取一个参数，如上所述，描述如下:

*   **值:**返回相反布尔值的给定值。

**返回值:**这个方法返回一个布尔值。

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装 lodash.js contrib 库。可以使用 **npm 安装 Lodash.js contrib 库-保存**。

**例 1:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

var bool = _.not( true ); 

console.log("Opposite boolean value 'true' is : ", bool);

var bool = _.not( false ); 

console.log("Opposite boolean value 'false' is : ", bool);
```

**输出:**

```
Opposite boolean value 'true' is : false
Opposite boolean value 'false' is : true
```

**例 2:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

var bool = _.not( 0 ); 

console.log("Opposite boolean value '0' is : ", bool);

var bool = _.not( 1 ); 

console.log("Opposite boolean value '1' is : ", bool);

var bool = _.not( 10 ); 

console.log("Opposite boolean value '10' is : ", bool);
```

**输出:**

```
Opposite boolean value '0' is : true
Opposite boolean value '1' is : false
Opposite boolean value '10' is : false
```

**例 3:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

var bool = _.not( {} ); 

console.log("Opposite boolean value empty object is : ", bool);

var bool = _.not( {'G' : "GeeksforGeeks"} ); 

console.log("Opposite boolean value object is : ", bool);

var bool = _.not( null ); 

console.log("Opposite boolean value 'null' is : ", bool);
```

**输出:**

```
Opposite boolean value empty object is : false
Opposite boolean value object is : false
Opposite boolean value 'null' is : true
```