# Lodash | _。取()法

> 原文:[https://www.geeksforgeeks.org/lodash-_-take-method/](https://www.geeksforgeeks.org/lodash-_-take-method/)

**_。take()方法**用于创建一个数组的切片，从开始有 n 个元素。

**语法:**

```
_.take(array, n)
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **Array:** This parameter stores the query array.
*   **n:** This parameter holds a number representing the number of elements to be obtained from the array.

**返回值:**这个方法返回前 n 个元素的数组。

**例 1:**

```
const _ = require('lodash');

let x = [1, 2, 'a', {'name': 'hello'}]

let newArray = _.take(x, 3);

console.log(newArray);
```

这里，`const _ = require('lodash')`用于将 lodash 库导入文件。

**输出:**

```
[ 1, 2, 'a' ]
```

**例 2:**

```
const _ = require('lodash');

let x = [
    {'name': 'lodash'}, 
    {'name': 'npm'}, 
    {'name': 'nodejs'}
]

let newArray = _.take(x, 2);

console.log(newArray);
```

**输出:**

```
[ { name: 'lodash' }, { name: 'npm' } ]

```

**例 3:**

```
const _ = require('lodash');

let x = [1, 2, 3, 4, 5, 6, 7]

let newArray = _.take(x, 5);

console.log(newArray);
```

**输出:**

```
[ 1, 2, 3, 4, 5 ]

```

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装库 lodash。

**参考:**T2】https://lodash.com/docs/4.17.15#take