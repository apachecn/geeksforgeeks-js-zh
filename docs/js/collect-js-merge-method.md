# Collect.js merge()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-merge-method/](https://www.geeksforgeeks.org/collect-js-merge-method/)

**合并()方法**用于将给定对象合并到原始集合中。如果给定对象的键与集合对象相同，则它会覆盖该键的值。

**语法:**

```
collect(array).merge(object)
```

**参数:**collect()方法获取一个参数，该参数被转换为集合，然后 merge()方法被应用于该参数。merge()方法将对象作为参数保存。

**返回值:**这个方法返回合并元素的集合。

**模块安装:**使用以下命令从项目根目录安装 *collect.js* 模块:

```
npm install collect.js
```

下面的示例说明了 collect.js 中的 merge()方法:

**示例 1:文件名:index.js**

## java 描述语言

```
// Requiring the module
const collect = require('collect.js');

let obj = ['Geeks', 'GeeksforGeeks'];

// Function call
const collection = collect(obj);

const merged_val = collection.merge(['Welcome', 'GFG']);

// Printing the merged collection
console.log(merged_val.all());
```

使用以下命令运行 **index.js** 文件:

```
node index.js
```

**输出:**

```
[ 'Geeks', 'GeeksforGeeks', 'Welcome', 'GFG' ]
```

**示例 2:文件名:index.js**

## java 描述语言

```
// Requiring the module
const collect = require('collect.js');

let obj = [
    {
        name: 'Rahul',
        dob: '25-10-96',
    },
    {
        name: 'Aditya',
        dob: '25-10-96',
    }
];

// Function call
const collection = collect(obj);

const merged_val = collection.merge({
    address: 'Noida',
    school: 'GeeksforGeeks',
});

// Printing the merged collection
console.log(merged_val.all());
```

使用以下命令运行 **index.js** 文件:

```
node index.js
```

**输出:**

```
[
  { name: 'Rahul', dob: '25-10-96' },
  { name: 'Aditya', dob: '25-10-96' },
  address: 'Noida',
  school: 'GeeksforGeeks'
]
```