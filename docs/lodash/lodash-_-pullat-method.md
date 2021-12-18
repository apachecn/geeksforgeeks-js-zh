# Lodash | _。pullAt()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-pullat-method/](https://www.geeksforgeeks.org/lodash-_-pullat-method/)

**_。pullAt()方法**用于移除给定地址对应的元素，并返回被移除元素的数组。

**语法:**

```
_.pullAt(array, arrayofIndexes)
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **Array:** This parameter stores the array to be modified.
*   **ArrayOfIndexes:** This parameter holds the index of the element to be removed from the array.

**返回值:**返回一个新的被移除元素的数组数组。

**示例 1:** 本示例从数组中移除给定的索引元素，并返回剩余元素的数组。

```
const _ = require('lodash');

let ar = [100, 200, 33, 400, 554]

let indexes = [1, 3, 4]

let value = _.pullAt(ar, indexes)

console.log('Original Array ', ar);

console.log('\nRemoved elements array ', value)
```

这里，`const _ = require('lodash')`用于将 lodash 库导入文件。

**输出:**

```
Original Array  [ 100, 33 ]

Removed elements array  [ 200, 400, 554 ]

```

**示例 2:** 本示例从数组中移除给定的索引元素，并返回剩余元素的数组。

```
const _ = require('lodash');

let ar = ['a', 'b', 'c', 'd', 'e']

let indexes = [1, 3]

let value = _.pullAt(ar, indexes)

console.log('Original Array ', ar);

console.log('\nRemoved elements array ', value)
```

**输出:**

```
Original Array  [ 'a', 'c', 'e' ]

Removed elements array  [ 'b', 'd' ]

```

**示例 3:** 本示例从数组中移除给定的索引元素，并返回剩余元素的数组。

```
const _ = require('lodash');

let ar = [{'name': 'lodash'}, 
          {'function': 'pullAt'}, 
          {'used on': 'array'}];

let indexes = [1, 2]

let value = _.pullAt(ar, indexes)

console.log('Original Array ', ar);

console.log('\nRemoved elements array ', value)
```

**输出:**

```
Original Array  [ { name: 'lodash' } ]

Removed elements array  [ { function: 'pullAt' }, { 'used on': 'array' } ]

```

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装库 lodash。

**参考:**T2】https://lodash.com/docs/4.17.15#pullAt