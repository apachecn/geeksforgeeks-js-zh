# 洛达什 _。每()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-every-method/](https://www.geeksforgeeks.org/lodash-_-every-method/)

Lodash 是一个工作在下划线. js 之上的 JavaScript 库。Lodash 有助于处理数组、集合、字符串、对象、数字等。_。每个方法检查谓词是否为集合的所有元素返回 true，一旦谓词错误地返回，迭代就停止。

**注意:**对于空集合，这个方法也返回 true，因为对于空集合的元素，一切都是真的。

**语法:**

```
_.every(collection, [predicate=_.identity])

```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **集合(数组|对象):**此参数保存要迭代的集合。
*   **【谓词=_。identity](函数):**此参数保存每次迭代调用的函数。

**返回值:**如果所有元素都通过谓词检查，则该方法返回 true，否则返回 false。

**示例 1:** 这里，const _ = require('lodash ')用于导入文件中的 lodash 库。

## JavaScript

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 

var obj1 = ([true, 1, null, 'yes']);
var obj2 = ([true, 2, 'active', 'yes']);

// Use of _.every() method

let x = _.every(obj1, Boolean);    
let y = _.every(obj2, Boolean);

// Printing the output 
console.log(x);
console.log(y);
```

**输出:**

```
false
true

```

**例二:**

## JavaScript

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 

var users = [ { 'user': 'jonny', 'age': 30, 'active': false }, 
              { 'user': 'harry', 'age': 35, 'active': false } ];

// Use of _.every() method
// The `_.matches` iteratee shorthand.

let x = _.every(users, { 'user': 'barney', 'active': false });

// Printing the output 
console.log(x);
```

**输出:**

```
false

```

**例三:**

## JavaScript

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 

var users = [
  { 'user': 'jonny', 'age': 30, 'active': false },
  { 'user': 'harry',  'age': 35, 'active': false }
];

// Use of _.every() method
// The `_.matchesProperty` iteratee shorthand.

let x = _.every(users, ['active', false]);

// Printing the output 
console.log(x);
```

**输出:**

```
true

```

**例 4:**

## JavaScript

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 

var users = [
  { 'user': 'jonny', 'age': 30, 'active': false },
  { 'user': 'harry',  'age': 35, 'active': false }
];

// Use of _.every() method
// The `_.property` iteratee shorthand.

let x = _.every(users, 'active');

// Printing the output 
console.log(x);
```

**输出:**

```
false

```

**注意:**这段代码在正常的 JavaScript 中无法工作，因为它需要安装库 lodash。