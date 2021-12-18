# D3.js 等分中心()方法

> 原文:[https://www.geeksforgeeks.org/d3-js-bisectcenter-method/](https://www.geeksforgeeks.org/d3-js-bisectcenter-method/)

**D3.js** 中的**平分中心()** **方法**用于返回数字数组中最接近给定值的值的索引。可以使用 *lo* 和 *hi* 参数来指定要考虑的阵列子集。

**语法:**

```
d3.bisectCenter( array, x, lo, hi )
```

**参数:**该方法接受上述四个参数，描述如下:

*   **Array:** is an array for evaluation.
*   **x:** is the value to be inserted.
*   **LO:** It defines the lower index of the array subset to be considered. This is an optional parameter.
*   **Hi:** Defines the higher index of the array subset to be considered. This is an optional parameter.

**返回值:**返回插入新元素后数组的索引。

**注意:**要执行以下示例，您必须安装 d3 库。下面的命令提示符我们必须执行下面的命令。

```
npm install d3
```

**例 1:** 在这个例子中，我们可以看到，通过使用这个方法，我们能够找到与数组中的值最接近的值的索引。

## Javascript

```
// Defining d3 contrib variable  
var d3 = require('d3');

var insert_index =
  d3.bisectCenter([1, 2, 3, 4, 5], 2);

console.log(insert_index);
```

**输出:**

```
1

```

**例 2:** 在这个例子中，我们可以看到，通过使用这个方法，我们能够找到数组中最接近浮点值的值的索引。

## Javascript

```
// Defining d3 contrib variable
var d3 = require("d3");

var arr =
  [0.2918, 0.0157, 0.637, 0.3536, 0.6813];

var insert_index =
  d3.bisectCenter(arr, 0.5);

console.log(insert_index);
```

**输出:**

```
2

```