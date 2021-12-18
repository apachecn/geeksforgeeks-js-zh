# Collect.js | diff()功能

> 原文:[https://www.geeksforgeeks.org/collect-js-diff-function/](https://www.geeksforgeeks.org/collect-js-diff-function/)

**diff()** **函数**将主集合与给定集合进行比较，并返回原始集合中但不在给定集合中的值。在 JavaScript 中，首先将数组转换为集合，然后将函数应用于集合。

**语法:**

```
data.diff(collection)

```

**参数:**该函数接受如上所述的单个参数，如下所述:

*   **收藏:**保存将与主收藏进行比较的收藏。

**返回值:**返回集合项之间有差异的新集合。

以下示例说明了**collect . js**
T5【示例 1: 中的 **diff()** 函数。在本例中，我们取一个集合，然后使用 **diff()** 函数并返回不在新集合中的值。

## java 描述语言

```
// It is used to import collect.js library
 const collect = require('collect.js');

const collection = collect([1, 2, 3, 4, 5 ,6]);
console.log(collection.diff([1, 2, 5]));
```

**输出:**

```
Collection { items: [ 3, 4, 6 ] }

```

**示例 2:** 有一点需要注意，这个函数保存了一个集合，与主集合进行比较，但只返回主集合中多余的那些项。

## java 描述语言

```
// It is used to import collect.js library
const collect = require('collect.js');

const col1 = [1, 2, 3, 4];
const col2 = [3, 4, 5, 6];

const x = collect(col1);
const y = collect(col2);

const difference = x.diff(y); 
console.log(difference.all());
```

**输出:**

```
[ 1 , 2]

```

**参考:**T2**https://collect.js.org/api/count.html**T5】