# Lodash | _。find()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-find-method/](https://www.geeksforgeeks.org/lodash-_-find-method/)

_。find()方法访问集合的每个值，并返回通过谓词真值测试的第一个元素，如果没有值通过测试，则返回 undefined。该函数一找到匹配项就返回。所以它实际上根据谓词搜索元素。
**语法:**

```
_.find(collection, predicate, fromIndex)
```

**参数:**该方法接受三个参数，如上所述，如下所述:

*   **集合:**此参数保存需要检查的数组或对象集合。
*   **谓词:**此参数保存迭代中调用的函数。
*   **从索引:**此参数保存您要开始搜索的索引(可选)。如果您没有传递这个参数，那么它会从头开始搜索。

**返回值:**返回匹配的元素，如果不匹配则返回未定义。
**例 1:** Tn 在这个例子中，我们将尝试找到第一个平方大于 100 的数字。

## java 描述语言

```
const _ = require('lodash');

let x = [2, 5, 7, 10, 13, 15];

let result = _.find(x, function(n) {
    if (n * n > 100) {
        return true;
    }
});

console.log(result);
```