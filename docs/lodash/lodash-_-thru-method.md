# 洛达什 _。通过()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-thru-method/](https://www.geeksforgeeks.org/lodash-_-thru-method/)

**Lodash** 是一个工作在下划线. js 之上的 JavaScript 库，Lodash 有助于处理数组、字符串、对象、数字等。

**_。*洛达什*中的**排序方法与*相似。tap()* 方法，唯一的区别是它返回拦截器的结果。此外，该方法主要用于通过替换中间结果来“传递”方法链序列中的值。

**语法:**

```
_.thru(value, interceptor)

```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **值:**是给拦截器的值。
*   **拦截器:**就是要调用的函数。

**返回值:**这个方法返回拦截器的结果。

**例 1:**

## Javascript

```
// Requiring lodash library
const _ = require('lodash');

// Calling thru() method
let result = _(144).thru(function(value) {
   return [value];
 }).value();

 // Displays output
 console.log(result);
```

**输出:**

```
[ 144 ]

```

**例二:**

## Javascript

```
// Requiring lodash library
const _ = require('lodash');

// Calling thru() method
let result = _('GfG').thru(function(value) {
   return [value];
 }).value();

 // Displays output
 console.log(result);
```

**输出:**

```
[ 'GfG' ]

```

**例三:**

## Javascript

```
// Requiring lodash library
const _ = require('lodash');

// Defining value
var val = ['g', 'f', 'G']

// Calling thru() method along with
// reverse and chain method
let result = _(val).reverse()
                   .chain()
                   .thru(function(value) {
    return [value];
 })
 .value();

 // Displays output
 console.log(result);
```

**输出:**

```
[ [ 'G', 'f', 'g' ] ]

```

这里，输出被反转，因为上面使用了 reverse()方法来反转所述值的顺序。

**参考:**T2】https://lodash.com/docs/4.17.15#thru