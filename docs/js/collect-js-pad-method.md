# Collect.js pad()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-pad-method/](https://www.geeksforgeeks.org/collect-js-pad-method/)

使用 **pad()方法**用给定的元素填充数组，直到数组的大小满为止。我们使用负尺寸填充元素左侧，使用正符号填充元素右侧。如果数组大小已满，则不会执行填充。

**语法:**

```
collect(array).pad(size, value)
```

**参数:**collect()方法接受一个参数，该参数被转换为集合，然后 pad()方法被应用于该参数。pad()方法保存两个参数，第一个是大小，另一个是值。

**返回值:**这个方法返回一个带有填充元素的数组列表。

**模块安装:**使用以下命令从项目根目录安装 *collect.js* 模块:

```
npm install collect.js
```

下面的例子说明了 collect.js 中的 pad()方法:

**示例 1:文件名:index.js**

## java 描述语言

```
// Requiring the module
const collect = require('collect.js');

// Creating collection object
const collection = collect(['Geeks', 'GFG', 'GeeksforGeeks']);

// Function call
const pad_val = collection.pad(5, 'Welcome');

// Printing values
console.log(pad_val.all());
```

使用以下命令运行 **index.js** 文件:

```
node index.js
```

**输出:**

```
[ 'Geeks', 'GFG', 'GeeksforGeeks', { G: 'Welcome' }, { G: 'Welcome' } ]
```

**示例 2:文件名:index.js**

## java 描述语言

```
// Requiring the module
const collect = require('collect.js');

// Creating collection object
const collection = collect(['Geeks', 'GFG', 'GeeksforGeeks']);

// Function call
const pad_val = collection.pad(-5, 'Welcome');

// Printing values
console.log(pad_val.all());
```

使用以下命令运行 **index.js** 文件:

```
node index.js
```

**输出:**

```
[ 'Welcome', 'Welcome', 'Geeks', 'GFG', 'GeeksforGeeks' ]
```