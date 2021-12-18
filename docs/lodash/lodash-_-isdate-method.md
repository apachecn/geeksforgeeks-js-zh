# 洛达什 _。isDate()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-isdate-method/](https://www.geeksforgeeks.org/lodash-_-isdate-method/)

洛达什 **_。方法** 检查给定值是否可以归类为日期对象。

**语法:**

```
_.isDate( Value )
```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **Value:** This parameter stores the value to be checked for the date object.

**返回值:**该方法返回一个**布尔值**(如果给定值是日期对象，则返回真，否则返回假)。

**例 1:**

```
// Defining Lodash variable
const _ = require('lodash'); 

var val = new Date;
// Checking for Date Object
console.log("The Value is Date : " 
            +_.isDate(val));
```

**输出:**

```
The Value is Date : true

```

**示例 2:** 以下示例返回 **false** ，因为该值是字符串对象，而不是日期对象。

```
// Defining Lodash variable
const _ = require('lodash'); 

var val = "15/07/2020";

// Checking for Date Object
console.log("The Value is Date : " 
            +_.isDate(val));
```

**输出:**

```
The Value is Date : false
```

**注意:** 这在正常的 JavaScript 中不会起作用，因为它需要安装 lodash 库。

可以使用 **npm 安装 lodash 来安装 Lodash 库。**T3】