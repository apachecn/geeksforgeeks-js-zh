# Collect.js only()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-only-method/](https://www.geeksforgeeks.org/collect-js-only-method/)

**only()方法**用于用指定的键返回给定集合中的项目。它将该键作为参数，并返回用该键映射的项。

**语法:**

```
collect(array).only(key)
```

**参数:**collect()方法接受一个转换为集合的参数，然后只对其应用()方法。唯一的()方法将键作为参数保存。

**返回值:**这个方法用指定的键返回给定集合中的项目。

**模块安装:**使用以下命令从项目根目录安装 *collect.js* 模块:

```
npm install collect.js
```

下面的示例说明了 collect.js 中的 only()方法:

**示例 1:文件名:index.js**

## java 描述语言

```
// Requiring the module
const collect = require('collect.js');

// Sample values array
let arr = [1, 2, 3, 4, 5, 6, 7, 8, 9];

// Creating collection object
const collection = collect(arr);

// Function call
const only_val = collection.only([2, 5, 25]);

// Printing the values
console.log(only_val.all());
```

使用以下命令运行 **index.js** 文件:

```
node index.js
```

**输出:**

```
[ 2, 5 ]
```

**示例 2:文件名:index.js**

## java 描述语言

```
// Requiring the module
const collect = require('collect.js');

// Creating collection object
const collection = collect({
    name: 'Rahul',
    dob: '25-10-96',
    section: 'A',
    score: 98,
});

// Function call
const only_val = collection.only(['name', 'dob']);

// Printing the values
console.log(only_val.all());
```

使用以下命令运行 **index.js** 文件:

```
node index.js
```

**输出:**

```
{ name: 'Rahul', dob: '25-10-96' }
```