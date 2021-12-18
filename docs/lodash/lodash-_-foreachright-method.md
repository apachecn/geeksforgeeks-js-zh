# 洛达什 _。forEachRight()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-foreachright-method/](https://www.geeksforgeeks.org/lodash-_-foreachright-method/)

洛达什 **_。forEachRight()** **方法**从右向左迭代集合的元素。它几乎和 _。forEach()方法。

**语法:**

```
_.forEachRight( collection, iteratee )

```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **集合:**此参数保存要迭代的集合。
*   **迭代:**是每次迭代调用的函数。

**返回值:**此方法返回集合。

**例 1:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.forEachRight() method 
_.forEachRight(['c', 'cpp', 'java',
      'python'], function(value) {
    console.log(value);
});
```

**输出:**

```
python
java
cpp
c

```

**例 2:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.forEachRight() method 
_.forEachRight({ 'x': 1, 'y': 2 }, 
    function(value, key) {
        console.log(key);
});
```

**输出:**

```
y
x

```

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装 lodash 库。
T3【参考:T5【https://lodash.com/docs/4.17.15#forEachRight】T6