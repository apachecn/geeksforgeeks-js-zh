# Collect.js | first()功能

> 原文:[https://www.geeksforgeeks.org/collect-js-first-function/](https://www.geeksforgeeks.org/collect-js-first-function/)

**first()** 函数给出集合的第一个值。简单地说，它返回第一个值，或者第一个方法返回集合中传递给定条件的第一个元素。在 JavaScript 中，首先将数组转换为集合，然后将函数应用于集合。

**语法:**

```
data.first(e)

```

**参数:**该函数接受如上所述的单个参数，如下所述:

*   **e** : this parameter must be held through a set.

的条件

**返回值:**已处理值

下面的例子说明了 collect.js 中的 **first()** 函数

**示例 1:** 在本例中，我们取一个集合，然后使用 **first()** 函数获取第一个值。

## Javascript

```
// It is used to import collect.js library

const collect = require('collect.js');

const nums = [0 , 1 , 2 , 3 , 4 , 5 , 6 , 7 , 8 , 9];
const data = collect(nums);

let value = data.first(e => e =4);
console.log(value);
```

**输出:**

```
0
```

**例 2:** 在本例中，我们将得到第一个负值。

## Javascript

```
// It is used to import collect.js library

const collect = require('collect.js');

const num = [0 , 1 , 2 , 3 , -4 , 5 , -6 , 7 , 8 , 9];
const data = collect(num);

let value = data.first(e => e < 0);
console.log(value);
```

**输出:**

```
-4
```

**参考:**T2**https://collect.js.org/api/first.html**T5】