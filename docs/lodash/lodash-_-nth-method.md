# Lodash | _。第(n)种方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-nth-method/](https://www.geeksforgeeks.org/lodash-_-nth-method/)

**_。第 n()方法**用于返回元素的第 n <sup>个</sup>索引。对于负值 n，它从末尾返回第 n 个<sup>元素。</sup>

**语法:**

```
_.nth(array, n)
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **Array:** This parameter stores the query array.
*   **n:** This parameter holds the index of the element to be extracted.

**返回值:**返回数组的第 n 个<sup>元素。</sup>

**示例 1:** 它返回数组的第三个元素。

```
const _ = require('lodash');

let ar = [1, 2, 3, 4, 5]

let value = _.nth(ar, 3)

console.log(value)
```

这里，`const _ = require('lodash')`用于将 lodash 库导入文件。

**输出:**

```
4
```

**示例 2:** 它返回数组末尾的第三个元素，因为 n 的值是负的。

```
const _ = require('lodash');

let ar = [1, 2, 3, 4, 5]

let value = _.nth(ar, -3)

console.log(value)
```

**输出:**

```
3
```

**示例 3:** 它返回 undefined，因为索引 8 处没有元素。

```
const _ = require('lodash');

let ar = [1, 2, 3, 4, 5]

let value = _.nth(ar, 8)

console.log(value)
```

**输出:**

```
undefined
```

**参考:**T2】https://lodash.com/docs/4.17.15#nth