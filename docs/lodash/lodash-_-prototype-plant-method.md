# Lodash _ prototype . plant()方法

> 原文:[https://www . geesforgeks . org/lo dash-_-原型-植物-方法/](https://www.geeksforgeeks.org/lodash-_-prototype-plant-method/)

**Lodash** 是一个工作在下划线. js 之上的 JavaScript 库，Lodash 有助于处理数组、字符串、对象、数字等。

*lodash* 中的 **_.prototype.plant(值)**序列方法用于通过将待种植的值作为包裹值种植来创建链序列类型的克隆。

**语法:**

```
_.prototype.plant(value)

```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **值:**是需要种植的值。

**返回值:**该方法返回新的 *lodash* 包装器实例。

**例 1:**

## Javascript

```
// Requiring lodash library
const _ = require('lodash');

// Creating an addition function
function add(n) {
  return n + n;
}

// Creating wrapped value
var wrapper = _([4, 4]).map(add);

// Calling prototype.plant(value) method
var res = wrapper.plant([8, 8]);

// Displays output 
console.log(res.value());
wrapper.value();
```

**输出:**

```
[ 16, 16 ]
[ 8, 8 ]

```

**例二:**

## Javascript

```
// Requiring lodash library
const _ = require('lodash');

// Creating a function
function fun(n) {
  return (n * 5);
}

// Calling prototype.plant(value) method
var obj = _().map(fun).plant({'f': 5, 'g': 7});

// Displays output 
console.log(obj.value());
```

**输出:**

```
[ 25, 35 ]

```

这里，值乘以 5，然后作为输出返回。

**参考:**T2】https://lodash.com/docs/4.17.15#prototype-plant