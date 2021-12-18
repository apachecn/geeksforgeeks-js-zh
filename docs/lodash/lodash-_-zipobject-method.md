# Lodash | _。zipObject()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-zipobject-method/](https://www.geeksforgeeks.org/lodash-_-zipobject-method/)

**_。zipOnject()方法**用于将两个数组组合成一个对象，一个数组作为键，另一个作为值。

**语法:**

```
_.zipObject([props=[]], [values=[]])
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **[道具=[]](数组):**此参数保存属性标识符。
*   **[values=[]](数组):**此参数保存属性值。

**返回值:**该方法返回一个包含给定数组对应键值的对象。

**例 1:**

## java 描述语言

```
const _ = require('lodash');

let x = ['a', 'b', 'c'];

let y = [1, 2, 3]

let obj = _.zipObject(x, y)

console.log(obj);
```

这里，const _ = require('lodash ')用于将 lodash 库导入文件。
**输出:**

```
{ a: 1, b: 2, c: 3 }
```

**例 2:**

## java 描述语言

```
const _ = require('lodash');

let x = ['name', ';language', 'used'];

let y = ['lodash', 'JavaScript', 'nodejs']

let obj = _.zipObject(x, y)

console.log(obj);
```

**输出:**

```
{ name: 'lodash', ';language': 'JavaScript', used: 'nodejs' }
```

**示例 3:** 如果您传递了一个额外的键，但没有值，它将放入与该键相关联的未定义值。

## java 描述语言

```
const _ = require('lodash');

let x = ['a', 'b', 'c', 'd'];

let y = [1, 2, 3]

let obj = _.zipObject(x, y)

console.log(obj);
```

**输出:**

```
{ a: 1, b: 2, c: 3, d: undefined }
```

**示例 4:** 如果您传递了一个额外的值，但没有键，它将忽略该值。

## java 描述语言

```
const _ = require('lodash');

let x = ['a', 'b', 'c'];

let y = [1, 2, 3, 4]

let obj = _.zipObject(x, y)

console.log(obj);
```

**输出:**

```
{ a: 1, b: 2, c: 3 }
```

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装库 lodash。
T3【参考:T5【https://lodash.com/docs/4.17.15#zipObject】T6