# Collect.js 中位数()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-median-method/](https://www.geeksforgeeks.org/collect-js-median-method/)

**中值()方法**用于从集合中返回集合元素的中值或给定键的中值。

**语法:**

```
collect(array).median(key)
```

**参数:**collect()方法接受一个参数，该参数被转换为集合，然后对其应用中值()方法。median()方法将键作为参数保存。

**返回值:**该方法返回集合元素的中值。

**模块安装:**使用以下命令从项目根目录安装 *collect.js* 模块:

```
npm install collect.js
```

下面的例子说明了 collect.js 中的中位数()方法:

**示例 1:文件名:index.js**

## java 描述语言

```
// Requiring the module
const collect = require('collect.js');

// Array containing sample values
let arr = [10, 15, -20, -25, 40, 50, -70];

// Creating collection object
const collection = collect(arr);

// Function call
const median_val = collection.median();

// Printing median value
console.log(median_val);
```

使用以下命令运行 **index.js** 文件:

```
node index.js
```

**输出:**

```
-25
```

**示例 2:文件名:index.js**

## java 描述语言

```
// Requiring the module
const collect = require('collect.js');

// Array containing sample values
let arr = [
  {
      name: 'Rahul',
      dob: '25-10-96',
      section: 'A',
      score: 98,
  },
  {
      name: 'Aditya',
      dob: '25-10-96',
      section: 'B',
      score: 96,
  },
  {
      name: 'Abhishek',
      dob: '16-08-94',
      section: 'A',
      score: 80
  }
];

// Creating collection object
const collection = collect(arr);

// Function call
const median_val = collection.median('score');

// Printing median value
console.log(median_val);
```

使用以下命令运行 **index.js** 文件:

```
node index.js
```

**输出:**

```
96
```