# 洛达什 _。赋值()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-assignin-method/](https://www.geeksforgeeks.org/lodash-_-assignin-method/)

洛达什 **_。**T2 就像那个 _。assign()方法，不同的是它迭代了自己的和继承的源属性。 后续源对象覆盖之前源的属性赋值。此方法变异对象。

**语法:**

```
_.assignIn( dest_object, [src_obj])

```

**参数:** 该方法接受两个参数，如上所述，描述如下:

*   **dest_object:** 这是目的对象。
*   **src_obj:** 这些是源对象。

**返回值:**这个方法返回一个对象。

**例 1:**

## java 描述语言

```
// Defining Lodash variable 
const _ = require('lodash'); 

function Gfg1() {
  this.a = 1;
}

function Gfg2() {
  this.c = 3;
}

Gfg1.prototype.b = 10;
Gfg2.prototype.d = 40;

console.log(_.assignIn( { a: 4 }, 
    new Gfg1, new Gfg2));
```

**输出:**

```
{ a: 1, b: 10, c: 3, d: 40 }
```

**例 2:**

## java 描述语言

```
// Defining Lodash variable 
const _ = require('lodash'); 

function Gfg1() {
  this.a = 1;
}

function Gfg2() {
  this.c = 3;
}

console.log(_.assignIn( { a: 4 }, 
    new Gfg1, new Gfg2));
```

**输出:**

```
{ a: 1, c: 3 }
```