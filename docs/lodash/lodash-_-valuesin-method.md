# 洛达什 _。值 In()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-valuesin-method/](https://www.geeksforgeeks.org/lodash-_-valuesin-method/)

**_。valuesIn()** **方法**用于返回对象的自身数组和继承的可枚举字符串键控属性值。

**语法:**

```
_.valuesIn(object)

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

// Use of _.valuesIn() method 
console.log(_.valuesIn(obj));
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

Fb.prototype.email = 'myself@gmail.com';

// Use of _.valuesIn() method 
console.log(_.valuesIn(new Fb));
```

**输出:**

```
[2045, "fb_myself", "fb1234", "myself@gmail.com"]

```