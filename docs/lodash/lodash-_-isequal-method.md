# 洛达什 _。isEqual()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-isequal-method/](https://www.geeksforgeeks.org/lodash-_-isequal-method/)

洛达什 **_。isEqual()方法** p 对两个值进行深度比较，以确定它们是否相等。此方法支持比较数组、数组缓冲区、布尔值、日期对象、映射、数字、对象、正则表达式、集合、字符串、符号和类型化数组。

**语法:**

```
_.isEqual( value1, value2)

```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **Value 1:** Value 1 is checked.
*   **Value 2:** Value 2 to be checked.

**返回值:**该方法返回一个**布尔值**(如果两个值相等则返回真，否则返回假)。

**例 1:**

## Javascript

```
// Defining Lodash variable 
const _ = require('lodash'); 

var val1 = { "a": "gfg" };

var val2 = { "a": "gfg" };

// Checking for Equal Value 
console.log("The Values are Equal : "
        +_.isEqual(val1,val2));
```

**输出:**

```
The Values are Equal : true

```

**例 2:** 为数组:

## **Javascript**

```
// Defining Lodash variable 
const _ = require('lodash'); 

var val1 = [1, 2, 3, 4]

var val2 = [1, 2, 3, 4]

// Checking for Equal Value 
console.log("The Values are Equal : "
        +_.isEqual(val1,val2));
```

****输出:****

```
The Values are Equal : true 
```

****例 3:** 为字符串:**

## ****Javascript****

```
**// Defining Lodash variable 
const _ = require('lodash'); 

var val1 = "gfg"

var val2 = "gfg"

// Checking for Equal Value 
console.log("The Values are Equal : "
        +_.isEqual(val1,val2));**
```