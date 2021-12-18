# Collect.js put()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-put-method/](https://www.geeksforgeeks.org/collect-js-put-method/)

**put()方法**用于设置集合中给定的键和值。

**语法:**

```
collect(array).put(key)
```

**参数:**collect()方法获取一个参数，该参数被转换为集合，然后 put()方法被应用于该参数。put()方法将键作为参数保存。

下面的例子说明了 collect.js 中的 put()方法:

**例 1:**

## Javascript

```
const collect = require('collect.js');

let obj = ['Geeks', 'GFG', 'GeeksforGeeks'];

const collection = collect(obj);

collection.put('Welcome');

console.log(collection.all());
```

**输出:**

```
[ 'Geeks', 'GFG', 'GeeksforGeeks', Welcome: undefined ]
```

**例二:**

## Javascript

```
onst collect = require('collect.js');

let obj = {
    name: 'Rahul',
    dob: '25-10-96',
    section: 'A',
    score: 98,
};

const collection = collect(obj);

collection.put(['Welcome to GeeksforGeeks']);

console.log(collection.all());
```

**输出:**

```
{
  name: 'Rahul',
  dob: '25-10-96',
  section: 'A',
  score: 98,
  'Welcome to GeeksforGeeks': undefined
}
```