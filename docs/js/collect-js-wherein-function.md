# collect . js WHere()函数

> 原文:[https://www.geeksforgeeks.org/collect-js-wherein-function/](https://www.geeksforgeeks.org/collect-js-wherein-function/)

whereIn()函数用于根据给定数组中包含的给定键或值来筛选集合。在 JavaScript 中，首先将数组转换为集合，然后将函数应用于集合。

**语法:**

```
data.whereIn('key')
```

**参数:**该函数接受如上所述的单个参数，如下所述:

*   **Key:** This parameter stores the key name that defines the key value.

**返回值:**返回带有所述键值的集合。

下面的例子说明了 collect.js 中的 whereIn()函数

**示例 1:** 在本例中，我们获取一个集合，然后使用 Here()方法，我们已经使用键返回了过滤后的集合。

## Javascript

```
// It is used to import collect.js library
const collection = collect([
  { Book: 'Let US C', price: 2000 },
  { Book: 'Begin Python', price: 1000 },
  { Book: 'Learn the DEV', price: 1500 },
]);

const filtered = collection.whereIn('price', [1000, 1500]);

filtered.all();
```

**输出:**

```
[
  { Book: 'Begin Python', price: 1000 },
  { Book: 'Learn the DEV', price: 1500 }
]
```

**例二:**

## Javascript

```
// It is used to import collect.js library
const collect = require('collect.js');

const Input = collect([
new Year('1980'),
new Year('2020'),
new Year('2025'),
]);

const output = Input.whereIn('Year',[2000, 2025]);

console.log(output.all());
```

**输出:**

```
[
  new Year('2025')
]
```

**参考:**T2】https://collect.js.org/api/whereIn.html