# 洛达什 _。mapArgsWith()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-mapargswith-method/](https://www.geeksforgeeks.org/lodash-_-mapargswith-method/)

洛达什 **_。mapArgsWith()** 方法接受一个映射函数，并返回一个新的组合函数，该函数将接受一个目标函数，并将在执行目标函数的主体之前返回一个将其参数与映射函数进行映射的新函数。

**语法:**

```
_.mapArgsWith( mapping_function );

```

**参数:**该方法接受如上所述的单个参数，定义如下:

*   **映射 _ 函数:**函数要接受的映射函数。

**返回值:**这个方法返回一个函数。

**注意:**要执行以下示例，您必须使用此命令提示符安装 **lodash-contrib** 库，并执行以下命令。

```
npm install lodash-contrib

```

以下示例说明了 Lodash _。JavaScript 中的 mapArgsWith()方法:

**示例 1:** 我们制作了一个函数，它对给定值进行立方运算，然后将该值与其自身相加。

## java 描述语言

```
// Defining lodash contrib variable
var _ = require('lodash-contrib'); 

function add (x) 
{ 
    return x + x + x ; }

function sub (x) 
{
    return  x - 2; 
}

var addnow = _.mapArgsWith(sub);

var subnow = addnow(add);

console.log(subnow(7))
```

**输出:**

```
15

```

**例 2:**

## java 描述语言

```
// Defining lodash contrib variable
var _ = require('lodash-contrib'); 

function squ (x) 
{ 
    return x * x ; }

function add (x) 
{
    return  x + 10; 
}

var addnow = _.mapArgsWith(add);

var sq = addnow(squ);

console.log(sq(5))
```

**输出:**

```
225

```

**例 3:**

## java 描述语言

```
// Defining lodash contrib variable
var _ = require('lodash-contrib'); 

function cs (x) 
{ 
    return "GeeksforGeeks : Computer Science Portal for Geeks" ; }

function geek (x) 
{
    return  "GeeksforGeeks"; 
}

var gfg = _.mapArgsWith(geek);

var gfgFunc = gfg(cs);

console.log(gfgFunc())
```

**输出:**

```
GeeksforGeeks : Computer Science Portal for Geeks

```

**例 4:**

## java 描述语言

```
// Defining lodash contrib variable
var _ = require('lodash-contrib'); 

function cs (x) 
{ 
    return x; }

function geek (x) 
{
    return  x[0]+" : "+x[1]; 
}

var gfg = _.mapArgsWith(geek);

var gfgFunc = gfg(cs);

console.log(gfgFunc(["GeeksforGeeks",
    "Computer Science Portal for Geeks"]))
```

**输出:**

```
GeeksforGeeks : Computer Science Portal for Geeks

```