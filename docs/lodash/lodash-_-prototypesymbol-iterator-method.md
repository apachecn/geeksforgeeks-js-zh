# 洛达什 _。原型[符号.迭代器]()方法

> 原文:[https://www . geesforgeks . org/lo dash-_-prototype symbol-iterator-method/](https://www.geeksforgeeks.org/lodash-_-prototypesymbol-iterator-method/)

**Lodash** 是一个工作在下划线. js 之上的 JavaScript 库，Lodash 有助于处理数组、字符串、对象、数字等。

**_。原型【符号.迭代器】()方法*中的序列***用于允许包装器*可迭代*。

**语法:**

```
_.prototype[Symbol.iterator]()

```

**参数:**此方法不接受任何参数。

**返回值:**该方法返回 *lodash* 包装对象。

**例 1:**

## Javascript

```
// Requiring lodash library
const _ = require('lodash');

// Creating wrapped variable
var wrapr = _([8, 9]);

// Calling [Symbol.iterator]() method
wrapr[Symbol.iterator]() === wrapr;

let obj = Array.from(wrapr);

// Displays output
console.log(obj);
```

**输出:**

```
[ 8, 9 ]

```

**例二:**

## Javascript

```
// Requiring lodash library
const _ = require('lodash');

// Creating wrapped variable
var wrapr = _(['Geeks', 'for', 'Geeks']);

// Calling [Symbol.iterator]() method
wrapr[Symbol.iterator]() === wrapr;

let obj = Array.from(wrapr);

// Displays output
console.log(obj);
```

**输出:**

```
[ 'Geeks', 'for', 'Geeks' ]

```

**例三:**

## Javascript

```
// Requiring lodash library
const _ = require('lodash');

// Calling [Symbol.iterator]() method and
// comparing it with wrapped value
_("Geeks")[Symbol.iterator]() === _("Geeks");

// Wrapper object
let obj = Array.from(_("Geeks"));

// Displays output
console.log(obj[0]);
console.log(obj[1]);
console.log(obj[2]);
console.log(obj[3]);
```

**输出:**

```
G
e
e
k

```

**参考:**T2】https://lodash.com/docs/4.17.15#prototype-Symbol-iterator