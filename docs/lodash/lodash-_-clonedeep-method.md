# Lodash | _。克隆 ep()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-clonedeep-method/](https://www.geeksforgeeks.org/lodash-_-clonedeep-method/)

**_。cloneDeep()方法**用于创建值的深度副本，即递归克隆值。这个方法类似于 _。clone()方法。

**语法:**

```
_.cloneDeep( value )
```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **Value:** This parameter holds the value to be recursively cloned.

**返回值:**该方法返回深度克隆值。

**示例 1:** 克隆简单对象

```
const _ = require('lodash');

var obj = {
    x: 23
};

// Deep copy
var deepCopy = _.cloneDeep(obj);

console.log('Comparing origianal with'
    + ' deep ', obj === deepCopy);

obj.x = 10; // Changing original value

console.log('After changing original value');

console.log("Original value ", obj);

console.log("Deep Copy value ", deepCopy);
```

**输出:**

```
Comparing origianal with deep  false
After changing original value
Original value  { x: 10 }
Deep Copy value  { x: 23 }
```

**示例 2:** 克隆复杂对象

```
const _ = require('lodash');

var obj = [{  x: 1 }, {y: 2}];

// Deep copy
var deepCopy = _.cloneDeep(obj);

console.log('Comparing origianal with deep ',
            obj[0] === deepCopy[0]);

// Changing orignal value
obj[0].x = 10;

// Values after changing original value
console.log("After changing original value");

console.log("Original value ", obj);

console.log("Deep Copy value ", deepCopy);
```

**输出:**

```
Comparing origianal with deep  false
After changing original value
Original value  [ { x: 10 }, { y: 2 } ]
Deep Copy value  [ { x: 1 }, { y: 2 } ]
```

因此，在这里我们已经看到，在改变原始值之后，值的深层副本没有改变，因为 _。cloneDeep()递归地深度复制了该值。

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装库 lodash。

**参考:**T2】https://lodash.com/docs/4.17.15#cloneDeep