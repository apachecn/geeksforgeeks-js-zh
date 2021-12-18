# Lodash | _。头()法

> 原文:[https://www.geeksforgeeks.org/lodash-_-head-method/](https://www.geeksforgeeks.org/lodash-_-head-method/)

**_。head()方法**用于获取数组的第一个元素。

**语法**

```
_.head( array )
```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **Array:** This parameter stores the query array.

**返回值:**返回数组的第一个元素。

**例 1:**

```
const _ = require('lodash');

let ar = [1, 2, 3, 4, 5]

let first = _.head(ar);

console.log(first)
```

**输出:**

```
1
```

**例 2:**

```
const _ = require('lodash');

let ar = [{a: 1, b: 2}, {c: 3, d:4}, {e: 5, f: 6}]

let first = _.head(ar);

console.log(first)
```

**输出:**

```
{ a: 1, b: 2 }
```

**例 3:**

```
const _ = require('lodash');

let ar = []

let first = _.head(ar);

console.log(first)
```

**输出:**

```
undefined

```

**注:** The _。空数组上的 head()方法返回 undefined。

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装库 lodash。

**参考:**T2】https://lodash.com/docs/4.17.15#head