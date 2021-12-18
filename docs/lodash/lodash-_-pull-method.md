# Lodash | _。拉()法

> 原文:[https://www.geeksforgeeks.org/lodash-_-pull-method/](https://www.geeksforgeeks.org/lodash-_-pull-method/)

**_。pull()方法**用于从给定数组中移除所有给定值。

**语法:**

```
_.pull(array, [values])
```

**参数:**该方法接受两个以上参数，如上所述，如下所述:

*   **Array:** This parameter stores the query array.
*   **Value:** This parameter holds one or more elements to be removed from the array.

**返回值:**返回一个包含剩余元素的数组。

**示例 1:** 本示例从数组中移除与给定值匹配的所有值。

```
const _ = require('lodash');

let ar = [1, 2, 3, 4, 5]

let value = _.pull(ar, 3, 5)

console.log(value)
```

这里，`const _ = require('lodash')`用于将 lodash 库导入文件。

**输出:**

```
[ 1, 2, 4 ]

```

**示例 2:** 本示例从数组中移除与给定值匹配的所有值。

```
const _ = require('lodash');

let ar = [1, 2, 3, 1, 3, 4, 1, 5]

let value = _.pull(ar, 1, 5)

console.log(value)
```

**输出:**

```
[ 2, 3, 3, 4 ]

```

**示例 3:** 本示例从数组中移除与给定值匹配的所有值。

```
const _ = require('lodash');

let ar = ['a', 'b', 'c', 'd']

let value = _.pull(ar, 'c')

console.log(value)
```

**输出:**

```
[ 'a', 'b', 'd' ]

```

**注意:**它在正常的 JavaScript 中不会工作，因为它需要安装库 lodash。

**参考:**T2】https://lodash.com/docs/4.17.15#pull