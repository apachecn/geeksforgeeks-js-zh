# 下划线. js _。千伏()法

> 原文:[https://www.geeksforgeeks.org/underscore-js-_-kv-method/](https://www.geeksforgeeks.org/underscore-js-_-kv-method/)

**_。kv()** 方法 r 返回对象中给定属性的键/值对，如果找不到则返回 undefined。

**语法:**

```
_.kv( Object_name, property );
```

**参数:**

*   **Object _ name:** The object to search for key/value pairs.
*   **Attribute:** The attribute that gives which given key/value pair to search.

**返回值:**这个方法 r 为给定的属性设置键/值对。

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装下划线. js contrib 库。

可以使用 **npm 安装下划线-contrib-save 来安装下划线. js contrib 库。**

**例 1:**

## Javascript

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var ob = { "gfg" : "GeeksforGeeks" };
var val = _.kv( ob, "gfg");

console.log(val);
```

**输出:**

```
[ 'gfg', 'GeeksforGeeks' ]
```

**例 2:** 如果没有找到键/值，这个方法返回 undefined。

## Javascript

```
// Defining underscore contrib variable
var _ = require('underscore-contrib'); 

var ob = { "gfg" : "GeeksforGeeks" };
var val = _.kv( ob, "geek");

console.log(val);
```

**输出:**

```
undefined
```