# 洛达什 _。truthy()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-truthy-method/](https://www.geeksforgeeks.org/lodash-_-truthy-method/)

**洛达什 _。truthy()方法**检查给定值是否 truthy，并返回相应的布尔值。真值是在布尔上下文中强制为真的值。

**语法:**

```
_.truthy( value );

```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **值:**要检查真实值的给定值。

**返回值:**如果给定值为真，则该方法返回布尔值 true，否则返回 false。

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装 lodash.js contrib 库。可以使用 **npm 安装 Lodash.js contrib 库。**

**例 1:**

## java 描述语言

```
// Defining underscore lodash variable 
var _ = require('lodash-contrib'); 

var bool = _.truthy(true); 
console.log("Given Value is True or not : ", bool);

var bool = _.truthy(false); 
console.log("Given Value is True or not : ", bool);
```

**输出:**

```
Given Value is True or not : true
Given Value is True or not : false

```

**例 2:**

## java 描述语言

```
// Defining underscore lodash variable 
var _ = require('lodash-contrib'); 

var bool = _.truthy(10); 
console.log("Given Value is True or not : ", bool);

var bool = _.truthy([10, 30, 50]); 
console.log("Given Value is True or not : ", bool);

var bool = _.truthy({"G" : "GeeksforGeeks"}); 
console.log("Given Value is True or not : ", bool);
```

**输出:**

```
Given Value is True or not : true
Given Value is True or not : true
Given Value is True or not : true

```