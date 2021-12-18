# 洛达什 _。rearg()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-rearg-method/](https://www.geeksforgeeks.org/lodash-_-rearg-method/)

**Lodash** 是一个工作在下划线. js 之上的 JavaScript 库，Lodash 有助于处理数组、字符串、对象、数字等。

**_。 *lodash* 中的 rearg()方法**用于创建一个调用*函数*参数的函数，参数根据所述索引组织。其中，第一个索引值的参数作为第一个参数发送，第二个索引值的参数作为第二个参数发送，依此类推。

**语法:**

```
_.rearg(func, indexes)

```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **函数:**是用来重组参数的函数。
*   **指标:**是有组织论证的指标。

**返回值:**该方法返回新函数。

**例 1:**

## Javascript

```
// Requiring lodash library
const _ = require('lodash');

// Calling rearg() method with its parameter
var fn = _.rearg(function(x, y, z) {
  return [x, y, z];
}, [2, 1, 0]);

// Calling fn
fn('z', 'y', 'x');
```

**输出:**

```
[ 'x', 'y', 'z' ]

```

**例二:**

## Javascript

```
// Requiring lodash library
const _ = require('lodash');

// Calling rearg() method with its parameter
var concat = _.rearg(function(Geeks, forGeeks) {
  return (Geeks+forGeeks);
}, [1, 0]);

// Calling concat
concat('forGeeks', 'Geeks');
```

**输出:**

```
GeeksforGeeks

```

**参考:**T2】https://lodash.com/docs/4.17.15#rearg