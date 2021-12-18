# Collect.js 分区()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-partition-method/](https://www.geeksforgeeks.org/collect-js-partition-method/)

**分区()方法**用于根据给定的回调函数分离集合元素。第一个数组包含满足谓词(条件)的元素，第二个数组包含剩余的元素。

**语法:**

```
collect(array).partition(callback)
```

**参数:**collect()方法接受一个参数，该参数被转换为集合，然后对其应用 partition()方法。partition()方法将回调函数作为参数保存。

**返回值:**这个方法返回带有分区的集合元素。

**模块安装:**使用以下命令从项目根目录安装 *collect.js* 模块:

```
npm install collect.js
```

下面的示例说明了 collect.js 中的 partition()方法:

**示例 1:文件名:index.js**

## java 描述语言

```
// Requiring the module
const collect = require('collect.js');

// Creating collection object
const collection = collect([1, 2, 3, 
    5, 6, 8, 9, 11, 17, 22]);

// Calling partition function on collection
const [odd, even] = collection.partition(
    element => element % 2 != 0);

// Printing the odd & even values
console.log(odd.all());
console.log(even.all());
```

使用以下命令运行 **index.js** 文件:

```
node index.js
```

**输出:**

```
[ 2, 6, 8, 22 ]
[ 1, 3, 5, 9, 11, 17 ]
```

**示例 2:文件名:index.js**

## java 描述语言

```
// Requiring the module
const collect = require('collect.js');

// Creating collection object
const collection = collect(['Welcome', 
    'Geeks', 'GFG', 'GeeksforGeeks']);

// Calling partition function on 
// collection object
const [short, long] = collection.partition(
    element => element.length < 6);

// Printing short values
console.log(short.all());

// Printing long values
console.log(long.all());
```

使用以下命令运行 **index.js** 文件:

```
node index.js
```

**输出:**

```
[ 'Geeks', 'GFG' ]
[ 'Welcome', 'GeeksforGeeks' ]
```