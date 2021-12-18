# Collect.js 转储()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-dump-method/](https://www.geeksforgeeks.org/collect-js-dump-method/)

collect.js 中的 **dump()** 方法用于打印特定时刻的数据，然后继续进一步执行代码。

**语法:**

```
collect.dump()
```

**参数:**不接受任何参数。

**返回值:**不返回值。

**例 1:**

## Javascript

```
// Importing the collect.js module
const collect = require('collect.js'); 
let array = ["a", "b", "c"];

// Making the collection
let collection= collect(array);

// Using dump() method to print
// the data at this moment
collection.dump()
```

**输出:**

```
Collection { items: [ 'a', 'b', 'c' ] }
```

**例二:**

## Javascript

```
// Importing the collect.js module.
const collect = require('collect.js');

let array = ["a", "b", "c", "d", "e"];

// Making the collection
let collection = collect(array);

// Using dump() method to print
// the data at this moment
collection.dump()
    .filter((v, k) => v >= "c")
    .dump()
```

**输出:**

```
Collection { items: [ 'a', 'b', 'c', 'd', 'e' ] }
Collection  { items: [ 'c', 'd', 'e' ] }
```

**参考:**T2】https://collect.js.org/api/dump.html