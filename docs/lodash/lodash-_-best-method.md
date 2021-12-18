# 洛达什 _。最佳()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-best-method/](https://www.geeksforgeeks.org/lodash-_-best-method/)

**洛达什 _。best()方法**取一个数组和一个函数，利用函数的条件从该数组中生成最佳合适的值。

**语法:**

```
_.best(array, function)

```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **数组:**计算最佳值的给定数组。
*   **函数:**包含最佳匹配值条件的函数。

**返回值:**此方法从数组中返回最佳值。

**注意:** 这在正常的 JavaScript 中无法工作，因为它需要安装 lodash contrib 库。

**模块安装:**可以使用以下命令安装 Lodash contrib 库:

```
npm install lodash-contrib –save
```

**示例 1:** 在本例中，我们将从数组中获取最佳值作为最大值。

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

// Array
var array = [11, 2, 43, 14, 12];

// Getting best value using best() method
var best_val = _.best(array, function(x, y) {
    return x > y;
});

console.log("Array : ", array);
console.log("Best value : ", best_val);
```

**输出:**

```
Array :  [ 11, 2, 43, 14, 12 ]
Best value :  43

```

**例 2:** 在本例中，我们将从数组中获取最佳值作为最小值。

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

// Array
var array = [11, 2, 43, 14, 12];

// Getting best value using best() method
var best_val = _.best(array, function(x, y) {
    return x < y;
});

console.log("Array : ", array);
console.log("Best value : ", best_val);
```

**输出:**

```
Array :  [ 11, 2, 43, 14, 12 ]
Best value :  2

```

**示例 3:** 在本例中，我们将从数组中获得最佳匹配值 12。

```
// Defining lodash contrib variable 
var _ = require('lodash-contrib'); 

// Array
var array = [11, 2, 43, 14, 12];

// Getting best value using best() method
var best_val = _.best(array, function(x) {
    return x == 12;
});

console.log("Array : ", array);
console.log("Best value : ", best_val);
```

**输出:**

```
Array :  [ 11, 2, 43, 14, 12 ]
Best value :  12

```