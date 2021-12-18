# 洛达什 _。克隆用()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-clonewith-method/](https://www.geeksforgeeks.org/lodash-_-clonewith-method/)

**Lodash** 是一个工作在下划线. js 之上的 JavaScript 库，Lodash 有助于处理数组、字符串、对象、数字等。

**_。***洛达什*中郎的**法与*相似。clone()* 方法，唯一不同的是它接受*定制器*，调用这个定制器是为了生成克隆值。此外，如果此处使用的*定制器*返回未定义，则克隆将改为由该方法处理。**

**注意:**这里用到的*定制器*最多可以用四个参数调用，分别是*值*、*索引|键*、*对象*、*栈*。

**语法:**

```
_.cloneWith(value, [customizer])

```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **Value:** is the value to be compared.
*   **Customizer:** is another value to be compared.

**返回值:**该方法返回克隆值。

**例 1:**

## Javascript

```
// Requiring lodash library
const _ = require('lodash');

// Creating a function customizer
function customizer(val) {
  if (_.isElement(val)) {
    return val.cloneNode(false);
  }
}

// Defining value parameter
var value = [1, 2, 3];

// Calling cloneWith() method
var cloned_value = _.cloneWith(value, customizer);

// Displays output
console.log(cloned_value);
```

**输出:**

```
[ 1, 2, 3 ]

```

**例二:**

## Javascript

```
// Requiring lodash library
const _ = require('lodash');

// Creating a function customizer
function customizer(val) {
  if (_.isElement(val)) {
    return val.cloneNode(false);
  }
}

// Defining value parameter
var value = ['Geeks', 'for', 'Geeks'];

// Calling cloneWith() method
var cloned_value = _.cloneWith(value, customizer);

// Displays output
console.log(cloned_value);
```

**输出:**

```
[ 'Geeks', 'for', 'Geeks' ]

```

**例 3:** 使用*集成器*()方法作为*定制器。*

## Javascript

```
// Requiring lodash library
const _ = require('lodash');

// Creating a function int which acts as
// customizer
function int(x) {
 if (_.isInteger(x)) {
   return true;
   }
}

// Calling cloneWith() method along with
// its parameter
var cloned_value = _.cloneWith({ gfg: 5, 
        geeksforgeeks: 6}, int);

// Displays output
console.log(cloned_value);
```

**输出:**

```
{ gfg: 5, geeksforgeeks: 6 }

```

**参考:**T2】https://lodash.com/docs/4.17.15#cloneWith