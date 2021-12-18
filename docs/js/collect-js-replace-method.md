# Collect.js replace()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-replace-method/](https://www.geeksforgeeks.org/collect-js-replace-method/)

**replace()方法**用于替换原始集合中与给定字符串或数字键匹配的元素。如果对象中给定的键与集合中的键匹配，则替换其值，否则，如果键不匹配，则将其添加到集合中。

**语法:**

```
collect(array).replace(object)
```

**参数:**collect()方法接受一个转换为集合的参数，然后对其应用 replace()方法。replace()方法将对象或元素作为参数保存。

**返回值:**该方法返回被替换值的集合元素。

下面的例子说明了 collect.js 中的 replace()方法:

**例 1:**

## java 描述语言

```
const collect = require('collect.js');

const collection =
  collect(['Geeks', 'GFG', 'GeeksforGeeks']);

const replaced =
  collection.replace({ 1: 'Welcome' });

console.log(replaced.all());
```

**输出:**

```
{ '0': 'Geeks', '1': 'Welcome', '2': 'GeeksforGeeks' }
```

**例 2:**

## java 描述语言

```
const collect = require('collect.js');

const collection = collect({
    name: 'Rahul',
    age: 25,
    section: 'A',
    marks: 88,
    address: 'Noida'
});

const replaced = collection.replace({
    name: 'Rajesh',
    marks: 45
});

console.log(replaced.all());
```

**输出:**

```
{ name: 'Rajesh', age: 25, section: 'A', marks: 45, address: 'Noida' }
```