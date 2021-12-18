# Lodash | _。fromPairs()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-frompairs-method/](https://www.geeksforgeeks.org/lodash-_-frompairs-method/)

**_。方法**返回一个由键值对组成的对象。这个方法是 _。toPairs()方法。

**语法:**

```
_.fromPairs( pairs )
```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **Pair:** This parameter holds the key-value pair of the array.

**返回值:**这个方法返回一个新的对象。

**例 1:**

```
const _ = require('lodash');

let pairs = [['x', 1], ['y', 2], ['z', 3]]

let obj = _.fromPairs(pairs);

console.log(obj)
```

**输出:**

```
{ x: 1, y: 2, z: 3 }

```

**例 2:**

```
const _ = require('lodash');

let pairs = [['one', 1], ['two', 2], ['three', 3]]

let obj = _.fromPairs(pairs);

console.log(obj)
```

**输出:**

```
{ one: 1, two: 2, three: 3 }

```

**例 3:**

```
const _ = require('lodash');

let pairs = [
    ['name', 'lodash'], 
    ['live', 'npm'], 
    ['used', 'nodejs']
]

let obj = _.fromPairs(pairs);

console.log(obj)
```

**输出:**

```
{ name: 'lodash', live: 'npm', used: 'nodejs' }

```

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装库 lodash。