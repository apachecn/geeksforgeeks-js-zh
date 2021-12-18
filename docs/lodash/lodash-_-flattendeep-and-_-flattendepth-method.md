# Lodash | _。flattenDeep()和 _。扁平化()方法

> 原文:[https://www . geeksforgeeks . org/lo dash-_-flappendeep-and-_-flappendepth-method/](https://www.geeksforgeeks.org/lodash-_-flattendeep-and-_-flattendepth-method/)

**洛达什 _。扁平化()方法**

**_。flattenDeep()方法**用于完全展平嵌套数组。它递归地这样做。

**语法:**

```
_.flattenDeep( array )
```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **数组:**此参数保存要展平的数组。

**返回值:**该方法返回新的展平数组。

**示例:**

```
const _ = require('lodash');

let ar = [1, [2, [3, 4, [5]]]];

let flattenArray = _.flattenDeep(ar);

console.log(flattenArray);
```

这里，`const _ = require('lodash')`用于将 lodash 库导入文件。

**输出:**

```
[ 1, 2, 3, 4, 5 ]

```

**洛达什 _。扁平化()方法**

**_。flattenDepth()方法**用于展平传递到函数中的深度时间。

**语法:**

```
_.flattenDepth(array, depth)
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **数组:**此参数保存需要展平的数组。
*   **深度:**此参数保存最大递归深度。

**返回值:**该方法返回新的展平数组。

**例 1:** 压平至深度 1

```
const _ = require('lodash');

let ar = [1, [2, [3, 4, [5]]]];

let flattenArray = _.flattenDepth(ar, 1);

console.log(flattenArray);
```

**输出:**

```
[ 1, 2, [ 3, 4, [ 5 ] ] ]

```

**例 2:** 压平至深度 2

```
const _ = require('lodash');

let ar = [1, [2, [3, 4, [5]]]];

let flattenArray = _.flattenDepth(ar, 2);

console.log(flattenArray);
```

**输出:**

```
[ 1, 2, 3, 4, [ 5 ] ]

```

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装库 lodash。

**参考:**

*   [https://lodash.com/docs/4.17.15#flattenDeep](https://lodash.com/docs/4.17.15#flattenDeep)
*   [https://lodash.com/docs/4.17.15#flattenDepth](https://lodash.com/docs/4.17.15#flattenDepth)