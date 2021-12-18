# 洛达什 _。entriesIn()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-entriesin-method/](https://www.geeksforgeeks.org/lodash-_-entriesin-method/)

**_。entriesIn()方法**用于为指定的对象创建自己的和继承的可枚举字符串键值对的数组。如果对象是地图或集合，则返回其条目。

**语法:**

```
_.entriesIn(object)
```

**参数:**该方法接受一个如上所述的参数，描述如下:

*   **Object:** This parameter stores the object to be queried.

**返回值:**该方法返回键值对。

**例 1:**

## Javascript

```
// Defining Lodash variable
const _ = require('lodash');

// Initializing a function gfg
function gfg() {
  this.a = 5;
  this.b = 10;
  this.c = 15;
}
gfg.prototype.d = 20;

// Calling the _.entriesIn() function
_.entriesIn(new gfg);
```

**输出:**

```
[ [ 'a', 5 ], [ 'b', 10 ], [ 'c', 15 ], [ 'd', 20 ] ]

```

**示例 2:** 在下面的代码中，集合用作对象，因此是 _。entriesIn()函数返回它的条目。

## Javascript

```
// Defining Lodash variable
const _ = require('lodash');

// Initializing a set
const object = {a: {b: 5}};

// Calling the _.entriesIn() function
_.entriesIn(object);
```

**输出:**

```
[ [ 'a', { b: 5 } ] ]

```

注意:这在普通的 JavaScript 中是行不通的，因为它需要安装 lodash 库。