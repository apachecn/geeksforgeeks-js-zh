# Collect.js max()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-max-method/](https://www.geeksforgeeks.org/collect-js-max-method/)

**max()方法**用于返回给定键的最大值。它接受一个集合，并返回该集合中给定键的最大值。

**语法:**

```
collect(array).max(key)
```

**参数:**collect()方法接受一个转换为集合的参数，然后对其应用 max()方法。max()方法可以保存对象的键。

**返回值:**此方法返回给定键的最大值。

**模块安装:**使用以下命令从项目根目录安装 *collect.js* 模块:

```
npm install collect.js
```

下面的示例说明了 collect.js 中的 max()方法:

**示例 1:文件名:index.js**

## java 描述语言

```
// Requiring the module
const collect = require('collect.js');

// Array with sample values
let arr = [10, 15, -20, -25, 40, 50, -70];

// Creating collection object
const collection = collect(arr);

// Function call
const max_val = collection.max();

// Printing the max value
console.log(max_val);
```

使用以下命令运行 **index.js** 文件:

```
node index.js
```

**输出:**

```
50
```

**示例 2:文件名:index.js**

## java 描述语言

```
// Requiring the module
const collect = require('collect.js');

// Array with sample values
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
const max_val = collection.max('score');

// Printing the max value
console.log(max_val);
```

使用以下命令运行 **index.js** 文件:

```
node index.js
```

**输出:**

```
98
```