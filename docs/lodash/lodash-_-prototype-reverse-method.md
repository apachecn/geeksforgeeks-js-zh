# Lodash _ prototype . reverse()方法

> 原文:[https://www . geesforgeks . org/lo dash-_-prototype-reverse-method/](https://www.geeksforgeeks.org/lodash-_-prototype-reverse-method/)

**Lodash** 是一个工作在下划线. js 之上的 JavaScript 库，Lodash 有助于处理数组、字符串、对象、数字等。

lodash 中的 Sequence 的 **_.prototype.reverse()方法**用于变异包装好的数组。而且，它是包装器版本的 _。数组的反向方法。

**语法:**

```
_.prototype.reverse()

```

**参数:**此方法不接受任何参数。

**返回值:**该方法返回新的 *lodash* 包装器实例。

**例 1:**

## Javascript

```
// Requiring lodash library
const _ = require('lodash');

// Creating an array of integers
var arr = [4, 5, 3];

// Calling _.prototype.reverse() method 
_(arr).reverse().value();

// Displays output
console.log(arr);
```

**输出:**

```
[ 3, 5, 4 ]

```

**例二:**

## Javascript

```
// Requiring lodash library
const _ = require('lodash');

// Creating an array of characters
var arr = ['a', 'b', 'c'];

// Calling _.prototype.reverse() method 
_(arr).reverse().value();

// Displays output
console.log(arr);
```

**输出:**

```
[ 'c', 'b', 'a' ]

```