# 洛达什 _。forOwnRight()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-forownright-method/](https://www.geeksforgeeks.org/lodash-_-forownright-method/)

洛达什 **_。forOwnRight()方法** 遍历给定对象的自己的键，调用  以相反的顺序为对象的每个属性迭代。使用三个参数调用迭代函数:(值、键、对象)。迭代函数可以通过显式返回 false 提前退出迭代。

**语法:**

```
_.forOwnRight( object, iteratee_function)

```

**参数:** 该方法接受两个参数，如上所述，描述如下:

*   **对象:**这是要查找的对象。
*   **迭代函数:**每次迭代调用的函数。

**返回值:**这个方法返回一个对象。

**例 1** :

## java 描述语言

```
// Defining Lodash variable 
const _ = require('lodash'); 

var users = {
  'a':  1,
  'b':  2,
  'c':  3
};

_.forOwnRight(users, function(value, key) {
  console.log(key, '=', value);
});
```

**输出:**

```
c = 3
b = 2
a = 1

```

**例 2:**

## java 描述语言

```
// Defining Lodash variable 
const _ = require('lodash'); 

var users = {
  'a':  1,
  'b':  2,
  'c':  3
};

_.forOwnRight(users, function(value, key) {
    if(value > 1){
        console.log(key, value);
    }
});
```

**输出:**

```
c 3
b 2

```

**注意:** 这在正常的 JavaScript 中不会起作用，因为它需要安装 lodash 库，可以使用 npm 安装 lodash 进行安装。