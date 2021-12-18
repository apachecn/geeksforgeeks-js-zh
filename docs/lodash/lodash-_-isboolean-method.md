# 洛达什 _。isBoolean()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-isboolean-method/](https://www.geeksforgeeks.org/lodash-_-isboolean-method/)

洛达什 **_。方法** 检查给定值是否可以归类为布尔值。

**语法:**

```
_.isBoolean( value )
```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **Value:** This parameter stores the Boolean value to be checked.

**返回值:**该方法返回一个**布尔值**(如果给定值是布尔值，则返回真，否则返回假)。

**示例 1:** T 当值为布尔值(真或假)时，他的方法返回 **true** 。

## Javascript

```
// Defining Lodash variable
const _ = require('lodash'); 

var val = true;

// Checking for Boolean
console.log("The Value is Boolean : " 
    +_.isBoolean(val));
```

**输出:**

```
The Value is Boolean : true
```

**例二:**

## Javascript

```
// Defining Lodash variable
const _ = require('lodash'); 

var val = false;

// Checking for Boolean
console.log("The Value is Boolean : " 
    +_.isBoolean(val));
```

**输出:**

```
The Value is Boolean : true
```

**例三:**

## Javascript

```
// Defining Lodash variable
const _ = require('lodash'); 

var val = null;

// Checking for Boolean
console.log("The Value is Boolean : "
    +_.isBoolean(val));
```

**输出:**

```
The Value is Boolean : false
```

**注意:** 这在正常的 JavaScript 中不会起作用，因为它需要安装 lodash 库。

可以使用 **npm 安装 lodash 来安装 Lodash 库。**T3】