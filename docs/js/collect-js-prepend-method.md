# Collect.js prepend()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-prepend-method/](https://www.geeksforgeeks.org/collect-js-prepend-method/)

**prepend()方法**用于在给定集合的开头添加一个项目。

**语法:**

```
collect(array).prepend(value)
```

**参数:**collect()方法接受一个转换为集合的参数，然后对其应用 prepend()方法。prepend()方法保存要添加到集合中的值。

**返回值:**该方法返回集合元素。

下面的例子说明了 collect.js 中的 prepend()方法:

**例 1:**

## java 描述语言

```
const collect = require('collect.js');

const collection = collect(['Geeks', 'GFG', 'GeeksforGeeks']);

collection.prepend('Welcome');

console.log(collection.all());
```

**输出:**

```
[ 'Welcome', 'Geeks', 'GFG', 'GeeksforGeeks' ]
```

**例 2:**

## java 描述语言

```
const collect = require('collect.js');

let obj = [
    {
        name: 'Rahul',
        dob: '25-10-96'
    },
    {
        name: 'Aditya',
        dob: '25-10-96'
    },
    {
        name: 'Abhishek',
        dob: '16-08-94'
    }
];

const collection = collect(obj);

collection.prepend({ name: 'Ashok', dob: '15-12-91' });

console.log(collection.all());
```

**输出:**

```
[
  { name: 'Ashok', dob: '15-12-91' },
  { name: 'Rahul', dob: '25-10-96' },
  { name: 'Aditya', dob: '25-10-96' },
  { name: 'Abhishek', dob: '16-08-94' }
]
```