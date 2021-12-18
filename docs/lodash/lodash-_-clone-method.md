# Lodash | _。克隆()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-clone-method/](https://www.geeksforgeeks.org/lodash-_-clone-method/)

**_。clone()方法**用于创建值的浅拷贝。此方法支持克隆数组、数组缓冲区、布尔值、日期对象、映射、数字、对象对象、正则表达式、集合、字符串、符号和类型化数组。它松散地基于结构化克隆算法。

**语法:**

```
_.clone( value )
```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **Value:** This parameter stores the value to be cloned.

**返回值:**该方法返回值的浅拷贝。

**示例 1:** 克隆简单对象

```
const _ = require('lodash');

var obj = {
    x: 23
};

// Shallow copy
var shallowCopy = _.clone(obj);

console.log('Comparing original with'
    + ' shallow ', obj === shallowCopy);

obj.x = 10; // Changing original value

console.log('After changing original value');

console.log("Original value ", obj);

console.log("Shallow Copy value ", shallowCopy);
```

这里，`const _ = require('lodash')`用于将 lodash 库导入文件。

**输出:**

```
Comparing original with shallow  false
After changing original value
Original value  { x: 10 }
Shallow Copy value  { x: 23 }
```

**示例 2:** 克隆复杂对象

```
const _ = require('lodash');

var obj = [{  x: 1 }, {y: 2}];

// Shallow copy
var shallowCopy = _.clone(obj);

console.log('Comparing original with shallow ',
            obj[0] === shallowCopy[0]);

// Changing orignal value
obj[0].x = 10;

// Values after changing original value
console.log("After changing original value");

console.log("Original value ", obj);

console.log("Shallow Copy value ", shallowCopy);
```

**输出:**

```
Comparing original with shallow  true
After changing original value
Original value  [ { x: 10 }, { y: 2 } ]
Shallow Copy value  [ { x: 10 }, { y: 2 } ]
```

所以，这里我们已经看到，在改变原始值之后，浅拷贝值也改变了，因为 _。clone()没有深度复制它只是传递了引用。

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装库 lodash。

**参考:**T2】https://lodash.com/docs/4.17.15#clone