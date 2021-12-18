# Collect.js | zip()功能

> 原文:[https://www.geeksforgeeks.org/collect-js-zip-function/](https://www.geeksforgeeks.org/collect-js-zip-function/)

**zip()** 函数用于将给定数组的值与给定索引处原始集合的值相结合。在 JavaScript 中，首先将数组转换为集合，然后将函数应用于集合。

**语法:**

```
data.zip(value)

```

**参数:**该函数接受如上所述的单个参数，如下所述:

*   **值:**该参数保存新数组中的值。**T3】**

**返回值:**按边距返回一个新集合，与主集合的值一一对应。

下面的示例说明了**collect . js:**
T5】示例 1: 中的 **zip()** 函数。在本例中，我们获取一个集合，然后使用 **zip()** 函数，使用 zip()方法将它们与新集合的相应项目数组进行匹配

## java 描述语言

```
// It is used to import collect.js library 
const collect = require('collect.js');

const fruits = collect(['Apple', 'Banana']);
const quantity = fruits.zip([10, 15]);

console.log(quantity.all());
```

**输出:**

```
[ Collection { items: [ 'Apple', 10 ] },
  Collection { items: [ 'Banana', 15 ] } ]

```

**例 2:**

## java 描述语言

```
// It is used to import collect.js library  
const collect = require('collect.js');

const people = collect(['Ram', 'Sham']);
const age = people.zip([20, 25]);

console.log(age.all());
```

**输出:**

```
[ Collection { items: [ 'Ram', 20 ] },
  Collection { items: [ 'Sham', 25 ] } ]

```

**参考:**T2**https://collect.js.org/api/zip.html**T5】