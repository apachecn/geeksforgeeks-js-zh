# 如何检查提供的值是否是 JavaScript 中指定的类型？

> 原文:[https://www . geeksforgeeks . org/如何检查提供的值是否是 javascript 中指定的类型/](https://www.geeksforgeeks.org/how-to-check-if-the-provided-value-is-of-the-specified-type-in-javascript/)

下面的方法介绍了如何检查提供的值是否是 JavaScript 中指定的类型。

**方法:**在 [**ECMAScript 2015**](https://www.geeksforgeeks.org/introduction-to-es6/) (通称 **ES6** )中介绍的 **Object.is()** JavaScript 方法判断两个值是否为同一个值。

**Object.is()** 判断两个值是否为同一个值。如果两个值都是未定义的，两个都是 null，两个都是 true 或两个都是 false，两个字符串长度相同，字符顺序相同，两个都是同一个对象(意味着两个值都引用内存中的同一个对象)，两个数字都是+0，都是-0，都是 [NaN，](https://www.geeksforgeeks.org/number-isnan-javascript/#:~:text=Return%20Value%3A-,The%20Number.,number%2Celse%20it%20returns%20false.&text=When%20an%20equation%20resulting%20in%20infinite%20value%20is%20passed%20as%20a%20parameter.&text=When%20a%20number%20is%20passed%20as%20a%20parameter.)或者都是非 0，都不是 NaN，都是相同的值

**语法:**

```
Object.is(value1, value2);
```

**参数:**该方法接受以下两个参数:

*   **Value 1:** is the value of the first comparison.
*   **Value 2:** is the value of the second comparison.

**返回值:**该函数返回布尔值。

**例 1:**

## index . js

```
// Evaluation result is the same as using ===
console.log(Object.is(25, 25));                // true
console.log(Object.is('foo', 'foo'));          // true
console.log(Object.is('foo', 'bar'));          // false
console.log(Object.is(null, null));            // true
console.log(Object.is(undefined, undefined));  // true
console.log(Object.is([], []));                // false

var foo = { a: 1 };
var bar = { a: 1 };

console.log(Object.is(foo, foo));              // true
console.log(Object.is(foo, bar));              // false
```

使用以下命令运行 **index.js** 文件:

```
node index.js
```

**输出:**

```
true
true
false
true
true
false
true
false
```

**例 2:**

## index . js

```
// Signed Zero
console.log(Object.is(0, -0));                 // false
console.log(Object.is(+0, -0));                // false
console.log(Object.is(-0, -0));                // true
console.log(Object.is(0n, -0n));               // true

// NAN case
console.log(Object.is(NaN, 0/0));              // true
console.log(Object.is(NaN, Number.NaN))        // true
```

使用以下命令运行 **index.js** 文件:

```
node index.js
```

**输出:**

```
false
false
true
true
true
true
```

**object . is()和===(严格相等)**

*   Object.is(+0，0)为假，Object.is(NaN，NaN)为真。
*   Therefore, Object.is () just = = = has different behaviors for negative zero -0 and [nan](https://www.geeksforgeeks.org/number-isnan-javascript/#:~:text=Return%20Value%3A-,The%20Number.,number%2Celse%20it%20returns%20false.&text=When%20an%20equation%20resulting%20in%20infinite%20value%20is%20passed%20as%20a%20parameter.&text=When%20a%20number%20is%20passed%20as%20a%20parameter.) .

**注意:**作为 ES6 的一个特性，它可能不被旧的浏览器支持，但是为了兼容性可以使用[巴贝尔](https://www.geeksforgeeks.org/reactjs-introduction-to-babel/)来实现。