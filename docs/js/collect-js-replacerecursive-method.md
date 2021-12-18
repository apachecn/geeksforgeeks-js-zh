# Collect.js replaceRecursive()方法

> 原文:[https://www . geesforgeks . org/collect-js-replace recursive-method/](https://www.geeksforgeeks.org/collect-js-replacerecursive-method/)

**replaceRecursive()方法**类似于 replace()方法，但是它递归地工作，并且该方法将递归到数组中，并且内部值用相同的替换过程处理。

**语法:**

```
collect(array).replaceRecursive(object)
```

**参数:**collect()方法接受一个转换为集合的参数，然后对其应用 replaceRecursive()方法。方法将对象或元素作为参数保存。

**返回值:**该方法返回被替换值的集合元素。

**模块安装:**使用以下命令从项目根目录安装 *collect.js* 模块:

```
npm install collect.js
```

下面的示例说明了 collect.js 中的 replaceRecursive()方法:

**示例 1:文件名:index.js**

## java 描述语言

```
// Requiring the module
const collect = require('collect.js');

// Creating collection object
const collection = collect([
    ['Geeks', 'GFG', 'GeeksforGeeks'], 
    ['Welcome', 'to', 'GeeksforGeeks']
]);

// Function call
const replaced = collection.replaceRecursive(
    { 0: 'Hello', 3: 'Welcome' });

// Printing values
console.log(replaced.all());
```

使用以下命令运行 **index.js** 文件:

```
node index.js
```

**输出:**

```
{
  '0': 'Hello',
  '1': { '0': 'Welcome', '1': 'to', '2': 'GeeksforGeeks' },
  '3': 'Welcome'
}
```

**示例 2:文件名:index.js**

## java 描述语言

```
// Requiring the module
const collect = require('collect.js');

const obj = [
    {
        name: 'Rahul',
        marks: 88
    },
    {
        name: 'Aditya',
        marks: 78
    },
    {
        name: 'Abhishek',
        marks: 87
    }
];

// Creating collection object
const collection = collect(obj);

// Function call
const replaced = collection.replaceRecursive(
    { 0: 'Welcome', 3: 'GeeksforGeeks' });

// Printing values
console.log(replaced.all());
```

使用以下命令运行 **index.js** 文件:

```
node index.js
```

**输出:**

```
{
  '0': 'Welcome',
  '1': { name: 'Aditya', marks: 78 },
  '2': { name: 'Abhishek', marks: 87 },
  '3': 'GeeksforGeeks'
}
```