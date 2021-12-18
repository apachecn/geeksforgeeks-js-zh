# Lodash _ prototype . at()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-prototype-at-method/](https://www.geeksforgeeks.org/lodash-_-prototype-at-method/)

**Lodash** 是一个工作在下划线. js 之上的 JavaScript 库，Lodash 有助于处理数组、字符串、对象、数字等。

*洛达什*中的 **_.prototype.at(【路径】)序列法**是**的包装版本。at()** 创建一个值数组的方法，该数组类似于对象的指定路径。

**语法:**

```
_.prototype.at([paths])

```

**参数:**该方法接受单个参数，如下所述:

*   **【路径】:**选择的是路径属性。

**返回值:**该方法返回新的 *lodash* 包装器实例。

**例 1:**

## Javascript

```
// Requiring lodash library
const _ = require('lodash');

// Creating an object variable
var obj = { 'x': [{ 'y': { 'z': 5 } }, 6] };

// Calling at() method 
let result = _(obj).at(['x[0].y.z', 'x[1]']).value();

// Displays output
console.log(result);
```

**输出:**

```
[ 5, 6 ]

```

**例二:**

## Javascript

```
// Requiring lodash library
const _ = require('lodash');

// Creating an object variable
var obj = { 'Geeks': [{ 'for': { 'Geeks': 5 } }, 13] };

// Calling at() method with its parameter
let result = _(obj).at(['Geeks[0].for.Geeks', 
            'Geeks[1]']).value();

// Displays output
console.log(result);
```

**输出:**

```
[ 5, 13 ]

```

**例三:**

## Javascript

```
// Requiring lodash library
const _ = require('lodash');

// Calling at() method with its parameter
let res = _({ 'b': { 'c': 33 } })
            .at(['b.c']).value();

// Displays output
console.log(res);
```

**输出:**

```
[ 33 ]

```

**参考:**T2】https://lodash.com/docs/4.17.15#prototype-at