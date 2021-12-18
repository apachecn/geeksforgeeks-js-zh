# 洛达什 _。福林()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-forin-method/](https://www.geeksforgeeks.org/lodash-_-forin-method/)

洛达什 **_。forIn()方法**迭代给定对象的键和值，并为每个属性调用迭代函数。迭代由三个参数调用:(值、键、对象)。迭代函数可以通过显式返回 false 提前退出迭代。

**语法:**

```
_.forIn( object, iteratee_function)

```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **对象:**这是要查找的对象。
*   **迭代函数:**每次迭代调用的函数。

**返回值:**这个方法返回一个对象。

**例 1** :

```
// Defining Lodash variable 
const _ = require('lodash'); 

var users = {
  'a':  1,
  'b':  2,
  'c':  3
};

_.forIn(users, function(value, key) {
  console.log(key);
});
```

**输出:**

```
a
b
c

```

**例 2:**

```
// Defining Lodash variable 
const _ = require('lodash'); 

var users = {
  'a':  1,
  'b':  2,
  'c':  3
};

_.forIn(users, function(value, key) {
    if(value > 1) {
        console.log(key, value);
    }
});
```

**输出:**

```
b 2
c 3

```

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装 lodash 库，并且可以使用以下命令进行安装:

```
npm install lodash
```