# 洛达什 _。keysIn()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-keysin-method/](https://www.geeksforgeeks.org/lodash-_-keysin-method/)

**_。keysIn()** **方法**用于创建对象的自身和继承的可枚举属性名称的数组。

**语法:**

```
_.keysIn(object)

```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **对象:**此参数保存要查询的对象元素。

**返回值:**这个方法返回给定对象的所有键的数组。

**例 1:**

## java 描述语言

```
/// Requiring the lodash library  
const _ = require("lodash");  

function Gfg() {
  this.a = 1;
  this.b = 2;
}

Gfg.prototype.c = 3;

// Use of _.keysIn method 
console.log(_.keysIn(new Gfg));
```

**输出:**

```
['a', 'b', 'c']

```

**例 2:**

## java 描述语言

```
/// Requiring the lodash library  
const _ = require("lodash");  

// Given object
var obj = { 
            Name: "GeeksforGeeks", 
            password: "gfg@1234", 
            username: "your_geeks"
        } 

// Use of _.keysIn method 
console.log(_.keysIn(obj));
```

**输出:**

```
["Name", "password", "username"]

```