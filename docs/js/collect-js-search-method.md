# Collect.js 搜索()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-search-method/](https://www.geeksforgeeks.org/collect-js-search-method/)

search()方法用于搜索集合中的给定元素，并返回其键(如果存在)。如果找不到该元素，则返回 false。

**语法:**

```
collect(array).search(element)
```

**参数:**collect()方法接受一个转换为集合的参数，然后对其应用 search()方法。search()方法保存要在集合中搜索的元素。

**返回值:**该方法返回元素存在的键，否则返回 false。

下面的例子说明了 collect.js 中的 search()方法:

**例 1:**

## Javascript

```
const collect = require('collect.js');

const collection = collect(
    ['Geeks', 'GFG', 'GeeksforGeeks']);

const searched = collection.search('GFG');

console.log(searched);
```

**输出:**

```
1
```

**例二:**

## Javascript

```
const collect = require('collect.js');

const collection = collect(['Geeks', 
    'GFG', 'GeeksforGeeks', 'Welcome']);

const searched = collection.search(
    element => element.length > 5);

console.log(searched);
```

**输出:**

```
2
```