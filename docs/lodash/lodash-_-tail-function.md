# Lodash | _。尾部()功能

> 原文:[https://www.geeksforgeeks.org/lodash-_-tail-function/](https://www.geeksforgeeks.org/lodash-_-tail-function/)

**_。tail()方法**用于创建不包含原始数组第一个元素的新数组。

**语法:**

```
_.tail( array )
```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **Array:** This parameter stores the query array.

**返回值:**这个方法返回数组的切片。

**例 1:**

```
const _ = require('lodash');

let x = [1, 2, 3, 4, 5, 6, 7]

let newArray = _.tail(x);

console.log(newArray);
```

这里，`const _ = require('lodash')`用于将 lodash 库导入文件。

**输出:**

```
[ 2, 3, 4, 5, 6, 7 ]

```

**例 2:**

```
const _ = require('lodash');

let x = [
    {'name': 'lodash'}, 
    {'name': 'npm'}, 
    {'name': 'nodejs'}
]

let newArray = _.tail(x);

console.log(newArray);
```

**输出:**

```
[ { name: 'npm' }, { name: 'nodejs' } ]

```

**例:**

```
const _ = require('lodash');

let x = [1, 2, 'a', {'name': 'hello'}]

let newArray = _.tail(x);

console.log(newArray);
```

**输出:**

```
[ 2, 'a', { name: 'hello' } ]

```

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装库 lodash。

**参考:**T2】https://lodash.com/docs/4.17.15#tail