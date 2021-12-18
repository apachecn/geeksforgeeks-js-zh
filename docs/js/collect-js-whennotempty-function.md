# Collect.js whenNotEmpty()函数

> 原文:[https://www . geesforgeks . org/collect-js-when notempty-function/](https://www.geeksforgeeks.org/collect-js-whennotempty-function/)

**Collect.js** 是一个流畅方便的包装器，用于处理数组和对象。**when notempty()**函数在集合不为空时执行回调函数。

**安装:**使用以下命令安装 **Collect.js** 模块:

```
npm install --save collect.js
```

**语法:**

```
collection.whenNotEmpty(callback)
```

**参数:**该函数只取一个参数，即如果集合不为空时执行的回调函数。

**返回值:**该函数返回新的集合对象。

**示例 1:Filename-index . js**

## Javascript

```
// Requiring module
const collect = require('collect.js')

// User defined collection
var myCollection = [
    'Good Morning', 
    'Good Evening', 
    'Good Afternoon'
]

// Creating collection object
const collection = collect(myCollection);

// Function call for single insertion
collection.whenNotEmpty(item => item.push('Good Night'));

// Printing collection
console.log(collection.all());
```

使用以下命令运行 **index.js** 文件:

```
node index.js
```

**输出:**

```
[ 'Good Morning', 'Good Evening', 'Good Afternoon', 'Good Night' ]
```

**示例 2:Filename-index . js**

## Javascript

```
// Requiring module
const collect = require('collect.js')

// User defined collection
var myCollection = ['One', 'Two', 'Three']

// Creating collection object
const collection = collect(myCollection);

// Function call for multiple insertion
collection.whenNotEmpty((item) => {
  item.push('Four')
  item.push('Five')
  item.push('Six')
});

// Printing collection
console.log(collection.all());
```

使用以下命令运行 **index.js** 文件:

```
node index.js
```

**输出:**

```
[ 'One', 'Two', 'Three', 'Four', 'Five', 'Six' ]
```

**参考:**T2】https://collect.js.org/api/whenNotEmpty.html