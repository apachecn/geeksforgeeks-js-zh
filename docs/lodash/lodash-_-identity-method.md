# 洛达什 _。身份()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-identity-method/](https://www.geeksforgeeks.org/lodash-_-identity-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、字符串、对象、数字等。_。 **identity** 方法返回收到的第一个参数。

**语法:**

```
_.identity(value)
```

**参数:**该方法接受一个参数，如上所述，如下所述:

*   **值:**可以是任意值。

**返回:**返回收到的第一个参数。

**例 1:**

```
// Requiring the lodash library  
const _ = require("lodash");        

// Use of _.identity() method   
var user = [
  { 'name': 'XXXX', 'age': 36, 'active': true },
  { 'name': 'YYYY',   'age': 40, 'active': false }
];

let gfg = _.identity(user);

// Printing the output  
console.log(gfg);
```

**注意:**这里，const _ = require('lodash ')用于导入文件中的 lodash 库。

**输出:**

```
[Object {active: true, age: 36, name: "XXXX"}, Object {active: false, age: 40, name: "YYYY"}]
```

**例 2:**

```
// Requiring the lodash library  
const _ = require("lodash");        

// Use of _.identity() method   
var company = { 'name': 'geeksforgeeks' };

let gfg = _.identity(company) === company;

// Printing the output  
console.log(gfg);
```

**注意:**这里，const _ = require('lodash ')用于导入文件中的 lodash 库。

**输出:**

```
true
```