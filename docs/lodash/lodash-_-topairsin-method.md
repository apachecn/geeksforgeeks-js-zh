# 洛达什 _。托帕辛()法

> 原文:[https://www.geeksforgeeks.org/lodash-_-topairsin-method/](https://www.geeksforgeeks.org/lodash-_-topairsin-method/)

**_。toPairsIn()** **方法**用于为对象创建一个自己的和继承的可枚举字符串键值对的数组，该数组可由 _。函数的作用是。如果对象是地图或集合，则返回其条目。

**语法:**

```
_.toPairsIn(object)

```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **对象:**此参数保存要查询的对象。

**返回值:**这个方法返回键值对的数组。

**例 1:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

function Fb() {
  this.id = 2045;
  this.username = 'fb_myself';
  this.password = 'fb1234';
}

Fb.prototype.email = 'myself@gmail.com';

// Use of _.toPairsIn() method 
console.log(_.toPairsIn(new Fb));
```

**输出:**

```
[
  [ 'id', 2045 ],
  [ 'username', 'fb_myself' ],
  [ 'password', 'fb1234' ],
  [ 'email', 'myself@gmail.com' ]
]
```

**例 2:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

function Gfg() {
  this.x = 1;
  this.y = 2;
}

Gfg.prototype.z = 3;

// Use of _.toPairsIn() method 
console.log(_.toPairsIn(new Gfg));
```

**输出:**

```
[ ['x', 1], ['y', 2], ['z', 3] ]
```

**例 3:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

var GfG = {
    "Geek": "GFG"
}

// Use of _.toPairsIn() method 
console.log(_.toPairsIn(GfG));
```

**输出:**

```
[ [ 'Geek', 'GFG' ] ]

```