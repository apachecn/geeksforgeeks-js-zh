# Lodash _ prototype . value()方法

> 原文:[https://www . geesforgeks . org/lo dash-_-prototype-value-method/](https://www.geeksforgeeks.org/lodash-_-prototype-value-method/)

**Lodash** 是一个工作在下划线. js 之上的 JavaScript 库，Lodash 有助于处理数组、字符串、对象、数字等。

**_.prototype.value()方法**用于执行给定的链序列，以解析展开的值。这个方法有别名 *_.prototype.toJSON* 和 *_.prototype.valueOf.*

**语法:**

```
_.prototype.value()

```

**参数:**此方法不接受任何参数。

**返回值:**该方法返回解析后的展开值。

**例 1:**

## Javascript

```
// Requiring lodash library
const _ = require('lodash');

// Using the _.prototype.value() method 
let result = _([5, 4, 7]).value();

// Display the result
console.log(result);
```

**输出:**

```
[ 5, 4, 7 ]

```

**例二:**

## Javascript

```
// Requiring lodash library
const _ = require('lodash');

// Defining values
let values = { "f":3, "g":15 };

// Using the _.prototype.value() method 
let unwrap_val = _(values).value();

// Display the result
console.log(unwrap_val);
```

**输出:**

```
{ f: 3, g: 15 }

```