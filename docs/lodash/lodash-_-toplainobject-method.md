# 洛达什 _。toPlainObject()方法

> 原文:[https://www . geesforgeks . org/lodash-_-toplainobject-method/](https://www.geeksforgeeks.org/lodash-_-toplainobject-method/)

**_。toPlainObject()方法**用于将指定的值转换为普通对象，将继承的可枚举字符串键控属性的值展平为普通对象的自有属性。

**语法:**

```
_.toPlainObject(value)

```

**参数:**该方法接受一个如上所述的参数，描述如下:

*   **Value:** This parameter holds a value to be converted.

**返回值:**该方法返回转换后的普通对象。

**例 1:**

## Javascript

```
// Defining Lodash variable
const _ = require('lodash');

// Initializing a function gfg()
function gfg() {
    this.a = 1;
}

// Calling _.toPlainObject() function
console.log(_.assign({ 'b': 2 }, 
    _.toPlainObject(new gfg)));
```

**输出:**

```
{ b: 2, a: 1 }

```

**例二:**

## Javascript

```
// Defining Lodash variable
const _ = require('lodash');

// Initializing a function gfg()
function gfg() {
     this.c = 4;
}
gfg.prototype.b = 2; 

// Calling _.toPlainObject() function
console.log( _.toPlainObject(new gfg) );
```

**输出:**

```
{ c: 4, b: 2 }

```

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装 lodash 库。