# 洛达什 _。defaultsDeep()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-defaultsdeep-method/](https://www.geeksforgeeks.org/lodash-_-defaultsdeep-method/)

**_。defaultsDeep()** **方法**递归分配默认属性。几乎和 _。默认值()函数。此方法使对象变异。

**语法:**

```
_.defaultsDeep(object, [sources])

```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **对象:**此参数保存目标对象。
*   **源:**该参数保存源对象。

**返回值:**该方法返回对象。

**例 1:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");

// Given object
var info = {
    Name: "GeeksforGeeks",
    password: "gfg@1234",
    username: "your_geeks"
}

// Use of _.defaultsDeep() method
console.log(_.defaultsDeep(info,
    _.defaults(info, { id: 'Id97' })));
```

**输出:**

```
{
  Name: 'GeeksforGeeks',
  password: 'gfg@1234',
  username: 'your_geeks',
  id: 'Id97'
}

```

**例 2:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");

// Use of _.defaultsDeep() method
console.log(_.defaultsDeep(
    {
        'x': { 'y': 20 }
    },
    {
        'x': { 'y': 10, 'z': 30 }
    }
)
);
```

**输出:**

```
{ 'x': { 'y': 20, 'z': 30 } }
```