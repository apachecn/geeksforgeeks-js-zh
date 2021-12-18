# 洛达什 _。第一现有()方法

> 原文:[https://www . geesforgeks . org/lodash-_-first existing-method/](https://www.geeksforgeeks.org/lodash-_-firstexisting-method/)

**洛达什 _。firstExisting()方法**从参数列表中返回第一个现有的参数。

**注意:**如果第一个参数不存在，如 null 或 undefined，此方法将忽略该参数并检查下一个。

**语法:**

```
_.firstExisting(arg1, arg2,....,argn);

```

**参数:**这个方法需要 n 个参数来检查第一个存在的参数。

**返回值:**这个方法返回第一个存在的参数。

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装 lodash.js contrib 库。可以使用 **npm 安装 lodash-contrib** 来安装 Lodash.js contrib 库。

**例 1:**

## java 描述语言

```
// Defining underscore lodash variable 
var _ = require('lodash-contrib'); 

var f_exist = _.firstExisting("gfg", "abc", 0, 1);

console.log("First Existing value is : ", f_exist);
```

**输出:**

```
First Existing value is : gfg

```

**例 2:**

## java 描述语言

```
// Defining underscore lodash variable 
var _ = require('lodash-contrib'); 

var f_exist = _.firstExisting(null, 
        undefined, "gfg", "abc", 0, 1);

console.log("First Existing value is : ", f_exist);
```

**输出:**

```
First Existing value is : gfg

```

**例 3:**

## java 描述语言

```
// Defining underscore lodash variable 
var _ = require('lodash-contrib'); 

var f_exist = _.firstExisting( 1, 2, 2, 3, 3, 4 );

console.log("First Existing value is : ", f_exist);
```

**输出:**

```
First Existing value is : 1

```