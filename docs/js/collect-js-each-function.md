# Collect.js |各()功能

> 原文:[https://www.geeksforgeeks.org/collect-js-each-function/](https://www.geeksforgeeks.org/collect-js-each-function/)

**每个()函数**遍历集合中的项目，并将每个项目传递给回调。在 JavaScript 中，首先将数组转换为集合，然后将函数应用于集合。

**语法:**

```
data.each(item)

```

**参数:**该函数接受如上所述的单个参数，描述如下:

*   **项目:**此参数保存将对项目上的集合执行任何操作的集合项目。

**返回类型:**执行定义运算符操作后返回结果。

下面的例子说明了 collect.js
**中的**每个()**函数示例 1:** 在这个例子中，我们取一个集合，然后使用每个()方法，我们对该集合应用+操作。

## java 描述语言

```
// It is used to import collect.js library
const collect = require('collect.js');

const num = [0 , 1 , 2 , 3 , 4];
let x = 0;
const data = collect(num);

data.each((item) => {
    x += item;
});

console.log(`sum = ${x}`);
```

**输出:**

```
sum = 10
```

**例 2:**

## java 描述语言

```
// It is used to import collect.js library
const collect = require('collect.js');

let sum = 0;
const collection = collect([1 , 5 , 7 , 9]);

collection.each((item) => {
  sum += item;
});

console.log(sum);
```

**输出:**

```
22
```

**参考:**T2**https://collect.js.org/api/each.html**T5】