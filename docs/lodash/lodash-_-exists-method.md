# 洛达什 _。存在()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-exists-method/](https://www.geeksforgeeks.org/lodash-_-exists-method/)

**洛达什 _。exists()方法**检查给定值是否为 Exist，并返回相应的布尔值。null 和 undefined 都被认为是不存在的值。所有其他值都是“Existy”。

**语法:**

```
_.exists( value );

```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **值:**要检查存在值的给定值。

**返回值:**如果给定值为 Existy，则该方法返回布尔值 true，否则返回 false。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装 lidash.js contrib 库。可以使用 **npm 安装 lodash-contrib** 来安装 Lodash.js contrib 库。

**例 1:**

## java 描述语言

```
// Defining underscore lodash variable 
var _ = require('lodash-contrib'); 

var bool = _.exists("Geeks");

console.log("Check the Existenc of Given Value : ", bool);
```

**输出:**

```
Check the Existenc of Given Value : true

```

**例 2:**

## java 描述语言

```
// Defining underscore lodash variable 
var _ = require('lodash-contrib'); 

var bool = _.exists(undefined); 

console.log("Check the Existenc of Given Value : ", bool);
```

**输出:**

```
Check the Existenc of Given Value : false

```

**例 3:**

## java 描述语言

```
// Defining underscore lodash variable 
var _ = require('lodash-contrib'); 

var bool = _.exists(null);

console.log("Check the Existenc of Given Value : ", bool);
```

**输出:**

```
Check the Existenc of Given Value : false

```

**例 4:**

## java 描述语言

```
// Defining underscore lodash variable 
var _ = require('lodash-contrib'); 

var bool = _.exists([1, 12, 2, 3]);

console.log("Check the Existenc of Given Value : ", bool);
```

**输出:**

```
Check the Existenc of Given Value : true

```