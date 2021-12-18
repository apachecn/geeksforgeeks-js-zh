# Collect.js | whereNotBetween()函数

> 原文:[https://www . geesforgeks . org/collect-js-where not between-function/](https://www.geeksforgeeks.org/collect-js-wherenotbetween-function/)

**whereNotBetween()** 功能用于过滤不在指定范围内的输入。在 JavaScript 中，首先将数组转换为集合，然后将函数应用于集合。
**语法:**

```
data.whereNotBetween(key, [range]);

```

**参数:**该函数接受两个参数，如上所述，如下所述:

*   **键:**该参数保存定义该键的值的键名。
*   **范围:**该参数保持指定的范围

**返回值:**返回不在该范围内的过滤集合。

下面的例子说明了 **collect.js:**
**中的 **whereNotBetween()** 函数示例 1:** 在本例中，我们取一个集合，然后使用 **whereNotBetween()** 方法指定一个键和值范围，以检查该值并返回不在该范围内的值。

## Javascript

```
// It is used to import collect.js library
const collect = require('collect.js');

const input= collect([
  { fruits: 'Apple', price: 200 },
  { fruits: 'Banana', price: 80 },
  { fruits: 'Papaya', price: 150 },
  { fruits: 'Grapes', price: 30 },
  { fruits: 'Cherry', price: 100 },
]);

const output = input.whereNotBetween('price', [100, 200]);
console.log(output.all());
```

**输出:**

```
[ { fruits: 'Banana', price: 80 },
  { fruits: 'Grapes', price: 30 } ]

```

**例 2:**

## java 描述语言

```
// It is used to import collect.js library
const collect = require('collect.js');

const input= collect([
  { quantity: 'Flour', price: 150 },
  { quantity: 'Rice', price: 100 },
  { quantity: 'Vegetables', price: 80 },
  { quantity: 'Fruits', price: 90 },
  { quantity: 'Pulses', price: 200 },
]);

const output = input.whereNotBetween('price', [90, 200]);
console.log(output.all());
```

**输出:**

```
[ { quantity: 'Vegetables', price: 80} ]

```

**参考:**T2**https://collect.js.org/api/whereNotBetween.html**T5】