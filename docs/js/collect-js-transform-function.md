# Collect.js | transform()函数

> 原文:[https://www . geesforgeks . org/collect-js-transform-function/](https://www.geeksforgeeks.org/collect-js-transform-function/)

**transform()函数**迭代一个集合，并回调集合中的每个项，集合中的项被新的回调值替换。它类似于 **[JavaScript map()函数](https://www.geeksforgeeks.org/javascript-array-map-method/)** ，但值在 **transform()函数**中被替换。
在 JavaScript 中，首先将数组转换为集合，然后将函数应用于集合。

**语法:**

```
data.transform(item, key)
```

**参数:**该函数接受两个参数，如上所述，如下所述:

*   **项:**此参数保存采集项。
*   **键:**该参数保存新的操作值。

**返回值:**返回由该函数创建的修改后的数组。

下面的例子说明了 collect.js 中的 **transform()函数**

**示例 1:** 在此示例中，我们采集一个集合，然后使用**变换()函数**使用**关键变换**参数修改值并返回新值。

```
// It is used to import collect.js library
const collect = require('collect.js');

const data= collect([1, 2, 3, 4, 5]);

data.transform((item, key) => item * 5);

console.log(data.all());
```

**输出:**

```
[5 , 10 , 15 , 20 , 25 ]
```

**示例 2:** 我们在这里做的事情与上面的示例相同。

```
// It is used to import collect.js library
const collect = require('collect.js');

const x= collect([10, 20, 30, 40, 50]);

x.transform((item, key) => item / 10);

console.log(x.all());
```

**输出:**

```
[1 , 2 , 3 , 4 , 5 ]
```

**参考:**T2】https://collect.js.org/api/transform.html