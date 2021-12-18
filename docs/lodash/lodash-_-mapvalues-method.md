# 洛达什 _。地图值()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-mapvalues-method/](https://www.geeksforgeeks.org/lodash-_-mapvalues-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、字符串、对象、数字等。

**_。mapValues()** 方法用于使用给定对象的相同键创建新的映射对象，并且使用给定的迭代函数生成值。

**语法:**

```
_.mapValues( object, iteratee )
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **对象:**此参数保存要迭代的对象。
*   **迭代:**该参数保存对象每次迭代调用的函数。它是一个可选值。

**返回值:**该方法返回新的映射对象。

**例 1:**

## java 描述语言

```
// Requiring the lodash library 
const _ = require("lodash"); 

var users = {
'Geeksforgeeks': {
    'username': 'gfg_id',
    'password': 'gfg@123'
  },
  'W3school': {
    'username': 'w3school_id',
    'password': 'w@123'
  }
};

// Using the _.mapValues() method
console.log(
  _.mapValues(users, function(o) {
    return o.password;
  })
);
```

**输出:**

```
{Geeksforgeeks: "gfg@123", W3school: "w@123"}
```

**例 2:**

## java 描述语言

```
// Requiring the lodash library 
const _ = require("lodash"); 

var users = {
  'Geeksforgeeks': {
    'username': 'gfg_id',
    'password': 'gfg@123'
  },
  'W3school': {
    'username': 'w3school_id',
    'password': 'w@123'
  }
};

// Using the _.mapValues() method
console.log(_.mapValues(users, 'password'));
```

**输出:**

```
{Geeksforgeeks: "gfg@123", W3school: "w@123"}
```