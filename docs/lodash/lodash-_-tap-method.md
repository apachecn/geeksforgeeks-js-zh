# 洛达什 _。tap()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-tap-method/](https://www.geeksforgeeks.org/lodash-_-tap-method/)

**Lodash** 是一个工作在下划线. js 之上的 JavaScript 库，Lodash 有助于处理数组、字符串、对象、数字等。

**_。tap()** **方法 *lodash* 中的**用于调用拦截器。此外，该方法的主要任务是“*”进入*”一个方法链序列，以便修改中间结果。

**语法:**

```
_.tap(value, interceptor)

```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **值:**是给拦截器的值。
*   **拦截器:**就是要调用的函数。

**返回值:**此方法返回值。

**例 1:**

## Javascript

```
// Requiring lodash library
const _ = require('lodash');

// Calling tap() method
let result = _([5, 6, 7]).tap(function(arr) {

   // Modifying input array using push
   // operation
   arr.push(8);
 })
.value();

 // Displays output
 console.log(result);
```

**输出:**

```
[ 5, 6, 7, 8 ]

```

**例二:**

## Javascript

```
// Requiring lodash library
const _ = require('lodash');

// Calling tap() method
let result = _(['Geeks', 'for']).tap(function(arr) {

   // Modifying input array using push
   // operation
   arr.push('Geeks');
   })
   .value();

 // Displays output
 console.log(result);
```

**输出:**

```
[ 'Geeks', 'for', 'Geeks' ]

```

**例 3:** 使用 *pop* 操作和 *tail* 方法。

## Javascript

```
// Requiring lodash library
const _ = require('lodash');

// Calling tap() method
let result = _(['f', 'g', 'h']).tap(function(arr) {

   // Modifying input array using pop
   // operation
   arr.pop();
 })
   .tail()     // Using tail() method
   .value();

 // Displays output
 console.log(result);
```

**输出:**

```
[ 'g' ]

```

**参考:**T2】https://lodash.com/docs/4.17.15#tap