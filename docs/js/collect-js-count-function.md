# Collect.js | count()功能

> 原文:[https://www.geeksforgeeks.org/collect-js-count-function/](https://www.geeksforgeeks.org/collect-js-count-function/)

**count()** 函数用于计算元素中集合的数量。在 JavaScript 中，首先将数组转换为集合，然后将函数应用于集合。

**语法:**

```
data.count()

```

**参数:**此函数不接受任何参数
**返回值:**返回该集合中元素的计数。

以下示例说明了 collect.js 中的 **count()** 功能
T3】示例 1:

## java 描述语言

```
// It is used to import collect.js library
const collect = require('collect.js');

const num = [0 , 1 , 2 , 3 , 4, 5 , 6, 7, 8, 9]; 
const data = collect(num);
const total = data.count();

console.log('Total number of elements are:', {total});
```

**输出:**

```
Total number of elements are: { total: 10 }

```

**例 2:**

## java 描述语言

```
// It is used to import collect.js library
const collect = require('collect.js');

const collection = collect([1, 2, 3, 4]);
const x = collection.count();

console.log(`Total number of elements are : ${x}`);
```

**输出:**

```
Total number of elements are : 4
```

**参考:**T2**https://collect.js.org/api/count.html**T5】