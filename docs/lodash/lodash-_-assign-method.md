# 洛达什 _。分配()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-assign-method/](https://www.geeksforgeeks.org/lodash-_-assign-method/)

Lodash 是一个工作在下划线. js 之上的 JavaScript 库，Lodash 有助于处理数组、字符串、对象、数字等。

**_。assign()** 方法用于将给定源对象的可枚举字符串键控属性分配给目标对象。源对象是从左到右应用的，任何后续源都会覆盖先前源的属性分配。

**语法:**

```
_.assign( dest_object, src_obj )

```

**参数:** 该方法接受两个参数，如上所述，描述如下:

*   **dest_object:** 这是目的对象。
*   **src_obj:** 这些是源对象。

**返回值:**这个方法返回一个对象。

**例 1:**

## Javascript

```
// Defining Lodash variable 
const _ = require('lodash'); 

// Using the ._assign() method
console.log(
  _.assign({ a: 1, c: 3 }, { a: 0 })
);
```

**输出:**

```
{ a: 0, c: 3 }

```

**例二:**

## Javascript

```
// Defining Lodash variable 
const _ = require('lodash'); 

// Using the ._assign() method
console.log(
  _.assign({ a: 0 }, { a: 1, c: 3 }, { d: 4 })
);
```

**输出:**

```
{ a: 1, c: 3, d: 4 }

```