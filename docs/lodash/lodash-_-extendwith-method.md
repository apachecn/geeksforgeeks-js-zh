# 洛达什 _。用()方法扩展

> 原文:[https://www.geeksforgeeks.org/lodash-_-extendwith-method/](https://www.geeksforgeeks.org/lodash-_-extendwith-method/)

**Lodash** 是一个工作在下划线. js 之上的 JavaScript 库，Lodash 有助于处理数组、字符串、对象、数字等。

**_。*洛达士*中【对象】的**方法**与*相似。assignIn()* 方法，唯一的区别是它接受*定制器*，调用这个定制器是为了生成赋值。此外，如果此处使用的*定制器*返回未定义，则该赋值改为由该方法处理。**

**注:**

*   The *customizer* used here can be called with five parameters, namely *objvalue* , [T4】 srcvvalue 【T5], *key* , *object* and *source* .
*   The objects used here are changed in this way.

**语法:**

```
_.extendWith(object, sources, [customizer])

```

**参数:**该方法接受三个参数，如上所述，如下所述:

*   **Object:** is the destination object.
*   **Source:** is the source object.
*   **Customizer:** is the function of customizing assignment.

**返回值:**这个方法返回一个对象。

**例 1:**

```
// Requiring lodash library
const _ = require('lodash');

// Defining a function customizer
function customizer(objectVal, sourceVal) {
  return _.isUndefined(objectVal) ? 
        sourceVal : objectVal;
}

// Calling extendWith method with its parameter
let obj = _.extendWith({ 'gfg': 1 }, 
        { 'geek': 3 }, customizer);

// Displays output
console.log(obj);
```

**输出:**

```
{ gfg: 1, geek: 3 }

```

**例 2:**

```
// Requiring lodash library
const _ = require('lodash');

// Defining a function customizer
function customizer(objectVal, sourceVal) {
  return _.isUndefined(objectVal) ? 
        sourceVal : objectVal;
}

// Defining a function GfG
function GfG() {
  this.p = 7;
}

// Defining a function Portal
function Portal() {
  this.r = 9;
}

// Defining prototype of above functions
GfG.prototype.q = 8;
Portal.prototype.s = 10;

// Calling extendWith method
// with its parameter
let obj = _.extendWith({ 'p': 6 }, 
    new GfG, new Portal, customizer);

// Displays output
console.log(obj);
```

**输出:**

```
{ p: 6, q: 8, r: 9, s: 10 }

```

**参考:**T2**https://lodash.com/docs/4.17.15#assignInWith**T5】