# Lodash | _。zipWith()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-zipwith-method/](https://www.geeksforgeeks.org/lodash-_-zipwith-method/)

**_。zipWIth()方法**用于通过在数组的相同索引处应用相同值的函数将数组组合成一个数组，首先将函数应用于数组的第一个值，然后将返回值添加到新的数组第一个值中，第二个、第三个也是如此，依此类推。如果你没有传递这个函数，它将简单地作为 zip 工作。

**语法:**

```
_.zipWith(arrays, [iteratee=_.identity])
```

**参数:**该方法接受两个或两个以上参数，如上所述，如下所述:

*   **Array:** This parameter holds one or more arrays to be processed.
*   **[iteration = _]. ID]:** This parameter holds the function of combining grouping values.

**返回值:**该方法在给定数组上应用函数后返回一个数组。

**例 1:**

```
const _ = require('lodash');

let x = [10, 20, 30];

let y = [100, 200, 300];

let combinedArray = _.zipWith(x, y, function(a, b) {
    return a + b;
});

console.log(combinedArray);
```

这里，`const _ = require('lodash')`用于将 lodash 库导入文件。

**输出:**

```
[ 110, 220, 330 ]

```

**例:**

```
const _ = require('lodash');

let x = [10, 20, 30];

let y = [100, 200, 300];

let z = [1000, 2000, 3000];

let combinedArray = _.zipWith(x, y, z, function(a, b, c) {
    return a + b + c;
});

console.log(combinedArray);
```

**输出:**

```
[ 1110, 2220, 3330 ]

```

**例:**

```
const _ = require('lodash');

let firstname = ['Rahul', 'Ram', 'Aditya'];

let lastname = ['Sharma', 'Kumar', 'Verma'];

let fullname = _.zipWith(firstname, lastname, function(a, b) {
    return a + ' ' + b;
});

console.log(fullname);
```

**输出:**

```
[ 'Rahul Sharma', 'Ram Kumar', 'Aditya Verma' ]

```

**例:**如果不传递函数，会和 _ 一样工作。zip()。

```
const _ = require('lodash');

let x = [10, 20, 30];

let y = [100, 200, 300];

let z = [1000, 2000, 3000];

let combinedArray = _.zipWith(x, y, z);

console.log(combinedArray);
```

**输出:**

```
[ [ 10, 100, 1000 ], [ 20, 200, 2000 ], [ 30, 300, 3000 ] ]

```

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装库 lodash。

**参考:**T2】https://lodash.com/docs/4.17.15#zipWith