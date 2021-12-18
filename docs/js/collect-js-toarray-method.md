# Collect.js toArray()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-toarray-method/](https://www.geeksforgeeks.org/collect-js-toarray-method/)

**toArray()方法**用于将给定集合转换为普通数组。如果集合是对象，将返回包含值的数组。

**语法:**

```
collect(array).toArray()
```

**参数:**collect()方法接受一个转换为集合的参数，并对其应用 toArray()方法。

**返回值:**这个方法返回一个给定集合的数组。

下面的例子说明了 collect.js 中的 toArray()方法:

**例 1:**

## java 描述语言

```
const collect = require('collect.js'); 

let arr = ['kripa', 'biltu', 'chinu', 1, 2, 3]; 

const collection = collect(arr); 

const newObject = collection.toArray(); 

console.log(newObject);
```

**输出:**

```
["kripa", "biltu", "chinu", 1, 2, 3]
```

**例 2:**

## java 描述语言

```
const collect = require('collect.js');

let obj =
{
    name: 'TATA',
    companies: [
        'tcs', 'tata motors',
        'tata tea', 'tata salt', 'sonata'
    ],
};

const collection = collect(obj);

const newObject = collection.toArray();

console.log(newObject);
```

**输出:**

```
[ 'TATA', [ 'tcs', 'tata motors', 'tata tea', 'tata salt', 'sonata' ] ]
```