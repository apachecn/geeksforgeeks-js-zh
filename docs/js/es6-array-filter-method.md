# ES6 |阵列滤波器()方法

> 原文:[https://www.geeksforgeeks.org/es6-array-filter-method/](https://www.geeksforgeeks.org/es6-array-filter-method/)

**数组过滤器()**是一个内置的方法，该方法创建一个新的数组，其元素遵循或通过给定的标准和条件。
为了更好地理解这一概念，下面仅举了几个例子

**语法:**

```
var newArray = arr.filter(callback(element[, index[, array]])
[, thisArg])
```

**参数:**该方法接受 2 个参数，上面提到过，下面描述:

*   **回调:**函数是一个谓词，用来测试数组的每个元素。返回 true 以保留元素，否则返回 false。它接受三个论点:
    *   **元素:**数组中正在处理的当前元素。
    *   **索引(可选):**数组中正在处理的当前元素的索引。
    *   **数组(可选):**调用了数组过滤器。
*   **该参数(可选):**执行回调时用作该参数的值。

**示例 1:** 过滤器功能过滤数组中所有大于 5 的数值

```
var numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
var result = numbers.filter(number => number > 5);
console.log(result);
```

**输出:**

```
[ 6, 7, 8, 9, 10 ]

```

**示例 2:** 过滤函数过滤数组中长度大于 5 的所有单词

```
var words = ["hi", "hello", "hey", "apple", "watermelon",
             "lemon", "javascript"];
var result = words.filter(word => word.length > 5);
console.log(result);
```

**输出:**

```
[ 'watermelon', 'javascript' ]

```

**示例 3:** 过滤函数从数组中过滤所有无效的用户 id。

```
var jsonarr = [
    {
        id: 1,
        name: "joe"
    },
    {
        id: -19,
        name: "john"
    },
    {
        id: 20,
        name: "james"
    },
    {
        id: 25,
        name: "jack"
    },
    {
        id: -10,
        name: "joseph"
    },
    {
        id: "not a number",
        name: "jimmy"
    },
    {
        id: null,
        name: "jeff"
    },
]

var result = jsonarr.filter(user => user.id > 0);

console.log(result);
```

**输出:**

```
[{"id":1,"name":"joe"},{"id":20,"name":"james"},
{"id":25,"name":"jack"}] 

```