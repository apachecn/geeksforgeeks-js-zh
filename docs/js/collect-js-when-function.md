# Collect.js | when()功能

> 原文:[https://www.geeksforgeeks.org/collect-js-when-function/](https://www.geeksforgeeks.org/collect-js-when-function/)

如果给定中的第一个参数被证明为真，则使用 **when()函数**进行回调。在 JavaScript 中，首先将数组转换为集合，然后将函数应用于集合。
**语法:**

```
data.when(conditional ,rule)

```

**参数:**该函数接受两个参数，如上所述，如下所述:

*   **规则:**此参数保存要应用于集合的操作规则或条件。**T3】**
*   **条件:**此参数保存条件值 true 或 false。

**返回值:**返回修改后的收藏列表。

下面的例子说明了**collect . js:**
T5【例 1: 中的 **when()** 函数在这个例子中，我们取一个集合，然后使用 **when()** 函数修改这个集合。

## java 描述语言

```
// It is used to import collect.js library   
const collect = require('collect.js');

const collection = collect([0 , 1 , 2]);
collection.when(true, items => items.push(3));

console.log(collection.all());
```

**输出:**

```
[0 , 1 , 2 , 3]

```

**示例 2:** 与上述示例相同，但应用不同的操作来执行。

## java 描述语言

```
// It is used to import collect.js library   
const collect = require('collect.js');

const collection = collect([0 , 1 , 2]);
collection.when(true, items => items.put('Jason'));

console.log(collection.all());
```

**输出:**

```
[ 0, 1, 2, Jason: undefined ]

```

**参考:**T2**https://collect.js.org/api/when.html**T5】