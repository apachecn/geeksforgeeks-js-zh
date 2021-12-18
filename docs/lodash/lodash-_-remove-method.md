# Lodash | _。移除()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-remove-method/](https://www.geeksforgeeks.org/lodash-_-remove-method/)

**_。remove()方法**用于从数组中移除谓词返回 True 并返回移除的元素的所有元素。

**语法:**

```
_.remove(array, function)
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **Array:** This parameter stores the array to be modified.
*   **Function:** This parameter holds the function called in each iteration.

**返回值:**返回一个移除元素的数组。

**例:**这里所有回归真的元素都是偶元素。在数组的所有元素(n)上调用该函数。

```
let x = [1, 2, 3, 4, 5];

let even = _.remove(x, function(n) {
    return n % 2 == 0;
});

console.log('Origianal Array ', x);
console.log('Removed element array ', even);
```

这里，`const _ = require('lodash')`用于将 lodash 库导入文件。

**输出:**

```
Origianal Array  [ 1, 3, 5 ]
Removed element array  [ 2, 4 ]

```

**示例 2:** 本示例从包含字母的数组中移除所有元音，并将它们存储在新数组中。

```
const _ = require('lodash');

let x = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i'];

let vowelArray = _.remove(x, function(n) {

    let vowels = ['a', 'e', 'i', 'o', 'u'];

    for (let i = 0; i < 5; i++)
    {
        if (n === vowels[i])
        {
            return true;
        }
    }
});

console.log(&#039;Origianal Array ', x);
console.log(&#039;Removed element array ', vowelArray);
```

**输出:**

```
Origianal Array  [ 'b', 'c', 'd', 'f', 'g', 'h' ]
Removed element array  [ 'a', 'e', 'i' ]

```

**示例 3:** 本示例从包含浮点数、字符和整数的给定数组中移除所有整数。

```
let x = ['a', 'b', 1, 5.6, 'e', -7, 'g', 4, 10.8];

let intsArray = _.remove(x, function(n) {

    return Number.isInteger(n);
});

console.log('Origianal Array ', x);
console.log('Removed element array ', intsArray);
```

**输出:**

```
Origianal Array  [ 'a', 'b', 5.6, 'e', 'g', 10.8 ]
Removed element array  [ 1, -7, 4 ]
```

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装库 lodash。

**参考:**T2】https://lodash.com/docs/4.17.15#remove