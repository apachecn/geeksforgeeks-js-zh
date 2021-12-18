# Collect.js | intersect()函数

> 原文:[https://www . geesforgeks . org/collect-js-intersect-function/](https://www.geeksforgeeks.org/collect-js-intersect-function/)

**intersect()** 函数用于移除给定集合中不存在的主集合中的值。在 JavaScript 中，首先将数组转换为集合，然后将函数应用于集合。

**语法:**

```
data.intersect('x')

```

**参数:**该函数接受如上所述的单个参数，如下所述:

*   **x:** 持有将与主集合相交的集合。

**返回值:**返回修改后的或者可以说相交的集合。

以下示例说明了**collect . js**
T5【示例 1: 中的 **intersect()** 函数。在本例中，我们获取一个集合，然后使用 **intersect()** 函数获取一个新集合，该集合与值相交，并返回修改后的集合。

## java 描述语言

```
// It is used to import collect.js library
const collect = require('collect.js');

const collection = collect([1, 2, 3, 4, 5]);
const any = collection.intersect([1, 2, 3, 9]);
console.log(any.all());
```

**输出:**

```
[ 1, 2, 3 ]

```

**例 2:**

## java 描述语言

```
// It is used to import collect.js library
const collect = require('collect.js');

const collection = collect([9 , 8 , 7 , 6 , 5]);
new1 = collection.intersect([6 , 5 , 8 , 4]);

console.log(new1.all());
```

**输出:**

```
[ 8, 6, 5 ]

```

**参考:**T2**https://collect.js.org/api/intersect.html**T5】