# Lodash _ prototype . chain()方法

> 原文:[https://www . geesforgeks . org/lo dash-_-prototype-chain-method/](https://www.geeksforgeeks.org/lodash-_-prototype-chain-method/)

**Lodash** 是一个工作在下划线. js 之上的 JavaScript 库，Lodash 有助于处理数组、字符串、对象、数字等。

*lodash* 中的 **_.prototype.chain()方法**用于创建带有启用的显式方法链序列的 *lodash* 包装器的实例。

**语法:**

```
_.prototype.chain()

```

**参数:**此方法不接受任何参数。

**返回值:**该方法返回新的 *lodash* 包装器实例。

**例 1:**

## Javascript

```
// Requiring lodash library
const _ = require('lodash');

// Initializing authors variable
var authors = [
  { 'author': 'Nidhi', 'articles': 750 },
  { 'author': 'Nisha', 'articles': 500 }
];

// Calling chain() method and creating
// an explicit chaining sequence
let result = _(authors).chain()
                       .tail()
                       .value();

// Displays output                       
console.log(result);
```

**输出:**

```
[ { author: 'Nisha', articles: 500 } ]

```

**例二:**

## Javascript

```
// Requiring lodash library
const _ = require('lodash');

// Initializing authors variable
var authors = [
  { 'author': 'Nidhi', 'articles': 750 },
  { 'author': 'Nisha', 'articles': 500 }
];

// Calling chain() method and creating
// an explicit chaining sequence
let result = _(authors).chain()
                       .head()
                       .pick('articles')
                       .value();

// Displays output                       
console.log(result);
```

**输出:**

```
{ articles: 750 }

```

**例三:**

## Javascript

```
// Requiring lodash library
const _ = require('lodash');

// Calling chain() method and creating
// an explicit chaining sequence
let obj = _("GeeksforGeeks").chain().value();

// Displays output                       
console.log(obj[0]);
console.log(obj[4]);
console.log(obj[7]);
console.log(obj[11]);
```

**输出:**

```
G
s
r
k

```

**参考:**T2】https://lodash.com/docs/4.17.15#prototype-chain