# 洛达什 _。forInRight()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-forinright-method/](https://www.geeksforgeeks.org/lodash-_-forinright-method/)

洛达什 **_。forInRight()方法**就像 _。方法，不同之处在于它使用迭代函数以相反的顺序迭代对象的属性。

**语法:**

```
_.forInRight( object, iteratee_function)

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

_.forInRight(users, function(value, key) {
  console.log(key);
});
```

**输出:**

```
c
b
a
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

_.forInRight(users, function(value, key) {
    if(value > 1) {
        console.log(key, value);
    }
});
```

**输出:**

```
c 3
b 2

```

**注意:**这在正常的 JavaScript 中无法工作，因为它需要安装 lodash 库，并且可以使用以下命令进行安装:

```
npm install lodash
```