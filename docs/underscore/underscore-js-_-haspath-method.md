# 下划线. js _。hasPath()方法

> 原文:[https://www . geesforgeks . org/下划线-js-_-haspath-method/](https://www.geeksforgeeks.org/underscore-js-_-haspath-method/)

**_。hasPath()** 方法 r 返回一个布尔值，指示在给定的键描述的路径上是否有属性。键可以以数组或点分隔字符串的形式给出。

**语法:**

```
_.hasPath( Object_name, key_string|array );
```

**参数:**

*   **对象名称:**要从中搜索值的对象。
*   **key_string | array:** 要在给定对象中搜索的给定点分隔字符串或数组。

**返回值:**这个方法 r 返回一个布尔值。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。

可以使用 **npm 安装下划线-contrib-save 来安装下划线. js contrib 库。**

**例 1:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var ob = { gfg : {
GeeksforGeeks :  "Computer Science Portal for Geeks"
            }
        };
var val = _.hasPath( ob, ['gfg','GeeksforGeeks'] );

console.log(val);
```

**输出:**

```
true
```

**例 2:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var ob = { gfg : {
    GeeksforGeeks :  "Computer Science Portal for Geeks"
            }
        };
var val = _.hasPath( ob, 'gfg.GeeksforGeeks');

console.log(val);
```

**输出:**

```
true
```

**例 3:**

## java 描述语言

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var ob = { gfg : {
GeeksforGeeks :  "Computer Science Portal for Geeks"
            }
        };
var val = _.hasPath( ob, 'gfg.Geeks');

console.log(val);
```

**输出:**

```
false
```