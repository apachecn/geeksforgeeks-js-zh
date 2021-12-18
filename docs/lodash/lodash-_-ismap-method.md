# 洛达什 _。isMap()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-ismap-method/](https://www.geeksforgeeks.org/lodash-_-ismap-method/)

洛达什 **_。isMap()方法**检查给定值是否为地图对象，并返回相应的布尔值。

**语法:**

```
_.isMap( value )

```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **值:**该参数保存地图对象需要检查的值。

**返回值:**该方法返回一个**布尔值**(如果给定值是地图对象，则返回真，否则返回假)。

**例 1:**

## java 描述语言

```
// Defining Lodash variable 
const _ = require('lodash'); 

var testMap = new Map;

// Checking for Map 
console.log("The Value is Map : "
        + _.isMap(testMap));
```

**输出:**

```
The Value is Map : true

```

**示例 2:** 对于 WeakMap 对象，此方法返回 false。

## java 描述语言

```
// Defining Lodash variable 
const _ = require('lodash'); 

var testMap = new WeakMap;

// Checking for Map 
console.log("The Value is Map : "
        + _.isMap(testMap));
```

**输出:**

```
The Value is Map : false

```

**例 3:** 对于字符串，返回 false。

## java 描述语言

```
// Defining Lodash variable 
const _ = require('lodash'); 

// Checking for Map 
console.log("The Value is Map : "
        + _.isMap("map"));
```

**输出:**

```
The Value is Map : false

```