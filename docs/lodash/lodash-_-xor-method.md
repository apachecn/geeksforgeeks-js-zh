# Lodash | _。异或()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-xor-method/](https://www.geeksforgeeks.org/lodash-_-xor-method/)

**_。xor()方法**返回一个给定数组的对称差的数组，即它将创建一个包含一个在任何其他数组中都不存在的元素的数组。

**语法:**

```
_.xor( arrays )
```

**参数:**该函数接受一个或多个参数，如上所述，如下所述:

*   **Array:** This parameter holds one or more arrays to be checked.

**返回值:**返回给定数组的对称差的数组。

**例 1:**

```
const _ = require('lodash');

let x = [3, 10, 100];

let y = [100, 10, 2];

let symmetricDifference = _.xor(x, y);

console.log(symmetricDifference);
```

这里，`const _ = require('lodash')`用于将 lodash 库导入文件。

**输出:**

```
[ 3, 2 ]

```

**例 2:**

```
const _ = require('lodash');

let x = [3, 10, 100];

let y = [100, 10, 2];

let z = [10, 500, 3];

let symmetricDifference = _.xor(x, y, z);

console.log(symmetricDifference);
```

**输出:**

```
[ 2, 500 ]

```

**例 3:**

```
const _ = require('lodash');

let js = ['web', 'mobile-app'];

let python = ['machine-learning', 'web'];

let c = ['basic-programming', 'system-app'];

let java = ['mobile-app', 'web', 'basic-programming'];

let symmetricDifference = _.xor(js, python, c, java);

console.log(symmetricDifference);
```

**输出:**

```
[ 'machine-learning', 'system-app' ]

```

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装库 lodash。

**参考:**T2】https://lodash.com/docs/4.17.15#xor