# Collect.js 隔()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-every-method/](https://www.geeksforgeeks.org/collect-js-every-method/)

**every()方法**用于验证给定集合的所有元素，并使用给定的真值测试。

**语法:**

```
collect(array).every()

```

**参数:**collect()方法接受一个转换为集合的参数，然后对其应用每个()函数，如果将它应用于对象集合，则可以接受元素。

下面的例子说明了 collect.js 中的 every()方法:

**例 1:**

## java 描述语言

```
const collect = require('collect.js');

const arr = [2, 4, 6, 8, 10, 12, 14];

const collection = collect(arr);

if (collection.every(element => element % 2 == 0)) {
    console.log('All elements are even');
} else {
    console.log('All elements are not even');
}
```

**输出:**

```
All elements are even

```

**例 2:**

## java 描述语言

```
const collect = require('collect.js');

const arr = ['Geeks', 'GFG', 'GeeksforGeeks', 'Welcome'];

const collection = collect(arr);

if (collection.every(element => element.length > 4)) {
    console.log('Every words contains more then 4 characters');
} else {
    console.log('Every words not contains more then 4 characters');
}
```

**输出:**

```
Every words not contains more then 4 characters

```