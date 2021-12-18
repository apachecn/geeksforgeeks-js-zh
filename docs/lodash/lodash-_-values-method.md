# 洛达什 _。数值()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-values-method/](https://www.geeksforgeeks.org/lodash-_-values-method/)

**_。values()** **方法**用于返回对象自身的可枚举字符串键控属性值的数组。

**语法:**

```
_.values(object)

```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **对象:**此参数保存要查询的对象。

**返回值:**这个方法返回对象元素的属性值数组。

**例 1:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// The source object
var obj = { 
    Name: "GeeksforGeeks", 
    password: "gfg@1234", 
    username: "your_geeks"
}

// Use of _.values() method 
console.log(_.values(obj));
```

**输出:**

```
["GeeksforGeeks", "gfg@1234", "your_geeks"]

```

**例 2:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// The source function
function Fb() {
  this.id = 2045;
  this.username = 'fb_myself';
  this.password = 'fb1234';
}

// This will not get included in values array
Fb.prototype.email = 'myself@gmail.com';

// Use of _.values() method 
console.log(_.values(new Fb)); 
console.log(_.values('GFG'));
```

**输出:**

```
[2045, "fb_myself", "fb1234"]
['G', 'F', 'G']

```