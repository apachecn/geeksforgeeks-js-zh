# Lodash _。bitwiseZ()方法〔t1〕

> 原文:[https://www.geeksforgeeks.org/lodash-_-bitwisez-method/](https://www.geeksforgeeks.org/lodash-_-bitwisez-method/)

**洛达什 _。方法**返回对所有参数使用> > >运算符的结果。

**语法:**

```
_.bitwiseZ( val1, val2,..., valn );

```

**参数:**该方法取 n 个值对其进行运算> > >运算符位次。

**返回值:**此方法返回对所有参数使用按位> > >运算符的结果。

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装 lodash.js contrib 库。可以使用 **npm 安装 Lodash.js contrib 库-保存**。

**例 1:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

var bZ  = _.bitwiseZ( 5 ); 

console.log("The bitwiseZ is :",bZ);
```

**输出:**

```
The bitwiseZ is : 5

```

**例 2:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

var bZ  = _.bitwiseZ( 1, 4, 6, 8 ); 

console.log("The bitwiseZ is :",bZ);
```

**输出:**

```
The bitwiseZ is : 0

```

**例 3:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

var bZ  = _.bitwiseZ( 72, 36 ); 

console.log("The bitwiseZ is :",bZ);
```

**输出:**

```
The bitwiseZ is : 4

```

**例 4:**

## java 描述语言

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

var bZ  = _.bitwiseZ( 72, 36, 2 ); 

console.log("The bitwiseZ is :",bZ);
```

**输出:**

```
The bitwiseZ is : 1

```