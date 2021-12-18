# Lodash | _。pullAll()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-pullall-method/](https://www.geeksforgeeks.org/lodash-_-pullall-method/)

**_。pullAll()方法**用于从第一个给定数组中移除第二个数组中给定的所有值。

**语法:**

```
_.pullAll(array, values)
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **Array:** This parameter stores the array to be modified.
*   **Value:** This parameter holds the value in the array that needs to be removed from the first array.

**返回值:**返回一个数组，该数组包含从第一个数组中移除的所有值。

**示例 1:** 本示例从第一个数组中移除第二个数组元素，并返回剩余的元素。

```
const _ = require('lodash');

let ar = [1, 2, 3, 4, 5]

let rem = [1, 3]

let value = _.pullAll(ar, rem)

console.log(value)
```

这里，`const _ = require('lodash')`用于将 lodash 库导入文件。

**输出:**

```
[ 2, 4, 5 ]
```

**示例 2:** 本示例从第一个数组中移除第二个数组元素，并返回剩余的元素。

```
const _ = require('lodash');

let ar = [1, 2, 3, 1, 3, 4, 1, 5]

let rem = [1, 4, 5]

let value = _.pullAll(ar, rem)

console.log(value)
```

**输出:**

```
[ 2, 3, 3 ]
```

**示例 3:** 本示例从第一个数组中移除第二个数组元素，并返回剩余的元素。

```
const _ = require('lodash');

let ar = ['a', 'b', 'c', 'd']

let rem = ['b', 'c']

let value = _.pullAll(ar, rem)

console.log(value)
```

**输出:**

```
[ 'a', 'd' ]

```

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装库 lodash。

**参考:**T2】https://lodash.com/docs/4.17.15#pullAll