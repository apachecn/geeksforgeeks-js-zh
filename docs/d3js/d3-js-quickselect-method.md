# D3.js 快速选择()方法

> 原文:[https://www.geeksforgeeks.org/d3-js-quickselect-method/](https://www.geeksforgeeks.org/d3-js-quickselect-method/)

**D3.js** 中的**快速选择()** **方法**用于以最快的方式对数组进行部分重新排序。

**语法:**

```
d3.quickselect( array, k, left, right, compare )

```

**参数:**该方法接受五个参数，如上所述，如下所述:

*   **数组:**是需要重新排序的数组。
*   **k:** 是要使用的重新排序值。
*   **左:**是数组中的左包含值。这是一个可选参数。
*   **右:**是数组中右包含值。这是一个可选参数。
*   **比较:**是用于数组中比较的函数。这是一个可选参数。

**返回值:**快速重排序后返回数组。

**注意:**要执行以下示例，您必须安装 d3 库。下面的命令提示符我们必须执行下面的命令。

```
npm install d3
```

**例 1:** 在这个例子中，我们可以看到，通过使用这个方法，我们能够在以最快的方式对数组进行重新排序后得到它。

## java 描述语言

```
// Defining d3 contrib variable  
var d3 = require('d3');

var reordered_array =
  d3.quickselect([3, 2, 1, 14, 5], 2);

console.log(reordered_array);
```

**输出:**

```
[ 1, 2, 3, 14, 5 ]

```

**示例 2:** 在本例中，我们使用 **Math.random()** 函数生成不同的值并将其存储在数组中。然后通过应用 **d3.quickselect()** 我们在数组中执行重新排序。

## java 描述语言

```
// Defining d3 contrib variable  
var d3 = require('d3');

var arr = [];
for(var i = 0; i < 5; i++) {
    arr.push(Math.random());
}

var reordered_array =
  d3.quickselect(arr, 4);

console.log(reordered_array);
```

**输出:**

```
[ 0.1504847356911596,
  0.42489989693286034,
  0.8801036441469585,
  0.5837860241062365,
  0.9175021021124463
]

```