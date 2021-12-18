# 洛达什 _。mapArgs()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-mapargs-method/](https://www.geeksforgeeks.org/lodash-_-mapargs-method/)

洛达什 **_。mapArgs()** 方法接受一个目标函数，并返回一个接受映射函数的新函数，该函数又返回一个函数，该函数将在调用原始目标函数之前映射其参数。

**语法:**

```
_.mapArgs( target_function, mapping_function );

```

**参数:**该方法接受两个参数，如上所述，定义如下:

*   **target_function:** 这个参数是调用的原函数。
*   **mapping_function:** 是函数要接受的映射函数。

**返回值:**这个方法返回一个函数。

**注意:**要执行以下示例，您必须使用此命令提示符安装 **lodash-contrib** 库，并执行以下命令。

```
npm install lodash-contrib

```

以下示例说明了 Lodash _。JavaScript 中的 mapArgs()方法:

**示例 1:** 我们制作了一个函数，它对给定值进行立方运算，然后将该值与其自身相加。

## java 描述语言

```
// Defining lodash contrib variable
var _ = require('lodash-contrib'); 

function add (x) 
{ 
    return x + x; }

function cube (x) 
{
    return  x * x * x; 
}

var cubethenadd = _.mapArgs(add)(cube);

console.log(cubethenadd(5))
```

**输出:**

```
250

```

**例 2:**

## java 描述语言

```
// Defining lodash contrib variable
var _ = require('lodash-contrib'); 

function add (x) 
{ 
    return x + x; }

function sub (x) 
{
    return  x - x; 
}

var subthenadd = _.mapArgs(add)(sub);

console.log(subthenadd(7))
```

**输出:**

```
0

```