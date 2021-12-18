# 洛达什 _。条目()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-entries-method/](https://www.geeksforgeeks.org/lodash-_-entries-method/)

**_。entries()方法**用于为指定的对象创建一个键值对数组。如果对象是地图或集合，则返回其条目。

**语法:**

```
_.entries(object)
```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **Object:** This parameter stores the object to be queried.

**返回值:**该方法返回键值对。

**例 1:**

## Javascript

```
// Defining Lodash variable
const _ = require('lodash');

// Specifying a function
function gfg() {
  this.A = 5;
  this.B = 10;
  this.C = 15;
}

// Calling the _.entries() function
_.entries(new gfg);
```

**输出:**

```
[ [ 'A', 5 ], [ 'B', 10 ], [ 'C', 15 ] ]
```

**例 2:** 在下面的代码中，一个集合作为对象，因此出现了 function _。entries()返回它的条目。

## 【JavaScript】

```
// Defining Lodash variable
const _ = require('lodash');

// Initializing a set
const object = {a: {b: 1}};

// Calling the _.entries() function
_.entries(object);
```

**输出:**

```
[ [ 'a', { b: 1 } ] ]
```

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装 lodash 库。