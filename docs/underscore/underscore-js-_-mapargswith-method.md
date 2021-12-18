# 下划线. js _。mapArgsWith()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-mapargswith-method/](https://www.geeksforgeeks.org/underscore-js-_-mapargswith-method/)

**_。mapArgsWith()** 方法采用一个映射函数，并返回一个新的组合函数，该函数将采用一个目标函数，并将返回一个新的函数，在执行目标函数的主体之前，用映射函数映射其参数。

**语法:**

```
_.mapArgsWith( mapping_function );
```

**参数:**

*   **映射 _ 函数:**函数要接受的映射函数。

**返回值:**这个方法 r 返回一个函数。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。

可以使用 **npm 安装下划线-contrib–save 来安装下划线. js contrib 库。**

**示例 1:** 我们制作了一个函数，它对给定值进行立方运算，然后将该值与其自身相加。

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

function add (x) { 
    return x + x + x ; 
}

function sub (x) {
    return  x - 2; 
}

var addnow = _.mapArgsWith(sub);

var subnow = addnow(add);

console.log(subnow(5))
```

**输出:**

```
9
```

**例 2:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

function squ (x) { 
    return x * x ; 
}

function add (x) {
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
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

function cs (x) { 
    return 
"GeeksforGeeks : Computer Science Portal for Geeks"; 
}

function geek (x) {
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
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

function cs (x) { 
    return x; 
}

function geek (x) {
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