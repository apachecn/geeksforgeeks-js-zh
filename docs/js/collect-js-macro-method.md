# Collect.js 宏()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-macro-method/](https://www.geeksforgeeks.org/collect-js-macro-method/)

**宏()方法**用于注册自定义方法。此方法使用了自定义函数。

**语法:**

```
collect(array).macro()
```

**参数:**collect()方法接受一个转换为集合的参数，然后对其应用宏()方法。

**返回值:**此方法返回集合键。

下面的例子说明了 collect.js 中的 macro()方法:

**例 1:**

## Javascript

```
const collect = require('collect.js');

collect().macro('even', function () {
    return this.map(element => element % 2 == 0);
});

const arr = [2, 3, 5, 6, 8, 9, 10, 12, 13, 16];

const collection = collect(arr);

console.log(collection.even());
```

**输出:**

```
Collection {
  items: [
    true, false, false,
    true, true,  false,
    true, true,  false,
    true
  ]
}
```

**例二:**

## Javascript

```
const collect = require('collect.js');

collect().macro('uppercase', function () {
    return this.map(element => element.toUpperCase());
});

const arr = ['gfg', 'geeks', 'GeeksforGeeks'];

const collection = collect(arr);

console.log(collection.uppercase());
```

**输出:**

```
Collection { items: [ 'GFG', 'GEEKS', 'GEEKSFORGEEKS' ] }
```