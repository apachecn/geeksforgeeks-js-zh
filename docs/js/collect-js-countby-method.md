# Collect.js countBy()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-countby-method/](https://www.geeksforgeeks.org/collect-js-countby-method/)

**countBy()方法**用于统计集合中值的出现次数。这个方法计算每个元素的出现次数。

**语法:**

```
collect(array).countBy()

```

**参数:**collect()方法接受一个转换为集合的参数，然后对其应用 countBy()方法。

**返回值:**该方法返回集合中值的出现次数。

下面的例子说明了 collect.js 中的 countBy()方法:

**例 1:**

## java 描述语言

```
// It is used to import collect.js library 
const collect = require('collect.js');

const num = [0, 1, 1, 2, 3, 4, 4, 5, 5, 5, 5, 5];
const data = collect(num);

const total = data.countBy();

console.log({ total });
```

**输出:**

```
{
 total: Collection {
   items: { '0': 1, '1': 2, '2': 1, '3': 1, '4': 2, '5': 5 }
 }
}

```

**例 2:**

## java 描述语言

```
const collect = require('collect.js');

const collection = collect([
    'geeks@gmail.com',
    'aman@gmail.com',
    'krk@gmail.com',
    'abc@gfg.com',
    'demo@gfg.com',
    'hr@geeksforgeeks.org'
]);

const counted = collection.countBy(
    email => email.split('@')[1]
);

console.log(counted.all());
```

**输出:**

```
{ 'gmail.com': 3, 'gfg.com': 2, 'geeksforgeeks.org': 1 }

```