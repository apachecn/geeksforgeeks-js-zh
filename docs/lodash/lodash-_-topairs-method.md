# 洛达什 _。toPairs()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-topairs-method/](https://www.geeksforgeeks.org/lodash-_-topairs-method/)

**_。toPairs()** **方法**用于为一个对象创建一个自己的可枚举字符串键值对数组，该数组可由 _。函数的作用是。如果对象是地图或集合，则返回其条目。

**语法:**

```
_.toPairs(object)

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

// This will not be included in the array
Fb.prototype.email = 'myself@gmail.com';

// Use of _.toPairs() method 
console.log(_.toPairs(new Fb));
```

**输出:**

```
[["id", 2045], ["username", "fb_myself"], ["password", "fb1234"]]

```

**例 2:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

var GfG = {
      'x': 1,
      'y': 2
 }

// Use of _.toPairs() method 
console.log(_.toPairs(GfG));
```

**输出:**

```
[['x', 1], ['y', 2]]

```