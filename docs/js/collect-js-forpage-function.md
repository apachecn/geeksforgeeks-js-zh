# Collect.js | forPage()函数

> 原文:[https://www.geeksforgeeks.org/collect-js-forpage-function/](https://www.geeksforgeeks.org/collect-js-forpage-function/)

**forPage()** 函数用于返回特定页面存在的值，该函数以页码为参数返回集合。在 JavaScript 中，首先将数组转换为集合，然后将函数应用于集合。

**语法:**

```
data.forPage(x,y)

```

**参数:**该函数接受两个参数，如上所述，如下所述:

*   **x:** 此参数保存页码。
*   **y:** 此参数保存每页显示的项目数。

**返回值:**返回新集合。

下面的例子说明了**collect . js**
T5【例 1: 中的 **forPage()** 函数在这个例子中，我们取一个集合，然后使用 **forPage()** 函数显示给定页面中作为参数的值，并返回该值

## java 描述语言

```
// It is used to import collect.js library 
const collect = require('collect.js');

const collection = collect([1, 2, 3, 4, 5, 6, 7, 8, 9]);
const Page= collection.forPage(2, 5);
console.log(Page.all());
```

**输出:**

```
[ 6, 7, 8, 9 ]

```

**例 2:**

## java 描述语言

```
// It is used to import collect.js library 
const collect = require('collect.js');

const collection = collect([1, 2, 3, 4, 5, 6, 7, 8, 9]);

const Page= collection.forPage(4, 2);
console.log(Page.all());
```

**输出:**

```
[ 7, 8 ]

```

**参考:**T2**https://collect.js.org/api/forPage.html**T5】