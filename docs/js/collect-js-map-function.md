# Collect.js | map()功能

> 原文:[https://www.geeksforgeeks.org/collect-js-map-function/](https://www.geeksforgeeks.org/collect-js-map-function/)

**map()** 函数迭代一个集合，并将每个值传递给回调。在 JavaScript 中，首先将数组转换为集合，然后将函数应用于集合。

**语法:**

```
data.map(rule)

```

**参数:**该函数接受如上所述的单个参数，如下所述:

*   **规则:**此参数保存要应用于集合的操作规则或条件。**T3】**

**返回值:**返回修改后的收藏列表。

下面的例子说明了 collect.js 中的 **map()** 函数

**示例 1:** 在此示例中，我们获取一个集合，然后使用 **map()** 函数将该操作应用于该集合。

## java 描述语言

```
// It is used to import collect.js library
const collect = require('collect.js');

const num = [1, 2, 3, 4, 5];

const data = collect(num);

const x = data.map(e => e * 3);

console.log(x.all());
```

**输出:**

```
[ 3, 6, 9, 12, 15 ]

```

**示例 2:** 与上述示例相同，但应用不同的操作来执行。

## 蟒蛇 3

```
//It is used to import collect.js library

const collect = require('collect.js');

const num = [10 ,20 ,30 ,40, 50];

const data = collect(num);

const x = data.map(e => e / 10);

console.log(x.all());
```

**输出:**

```
[1 , 2, 3 ,4 ,5]

```

**参考:**T2**https://collect.js.org/api/map.html**T5】