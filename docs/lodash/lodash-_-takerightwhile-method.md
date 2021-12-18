# 洛达什 _。takeRightWhile()方法

> 原文:[https://www . geeksforgeeks . org/lodash-_-takentrightwhile-method/](https://www.geeksforgeeks.org/lodash-_-takerightwhile-method/)

_。takeRightWhile 方法用于创建数组的一个切片，在这个切片中，从末尾获取元素，这些元素一直被获取，直到谓词错误地返回。

**语法:**

```
_.takeRightWhile(array, [predicate=_.identity])

```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **Array:** This parameter stores the array to be queried.
*   **[predicate = _]. Identity]:** This parameter holds the function called in each iteration.

**返回值:**此方法用于返回数组的切片。

**示例 1:** 这里，const _ = require('lodash ')用于导入文件中的 lodash 库。

## JavaScript

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var users = [{ 'user': 'fred',    'active': false 

},
  { 'user': 'pebbles', 'active': false }];

// Use of _.takeRightWhile() 
// method 
let ind = _.takeRightWhile(users, function(o) { 

return !o.active; }); 

// Printing the output 
console.log(ind);
```

**输出:**

```
[{ user: 'fred', active: false }, {user: 'pebbles', active: false}]

```

**例二:**

## JavaScript

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var users = [{ 'user': 'fred',    'active': false 

},
  { 'user': 'pebbles', 'active': false }];

// Use of _.takeRightWhile() 
// method 
// The `_.matches` iteratee shorthand.
let gfg = _.takeRightWhile(users, { 'user': 

'pebbles', 'active': false }); 

// Printing the output 
console.log(gfg);
```

**输出:**

```
[{user: 'pebbles', active: false}]

```

**例三:**

## JavaScript

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var users = [{ 'user': 'fred',    'active': false 

},
  { 'user': 'pebbles', 'active': false }];

// Use of _.takeRightWhile() 
// method
// The `_.matchesProperty` iteratee shorthand.

let gfg = _.takeRightWhile(users, ['active', 

false]); 

// Printing the output 
console.log(gfg);
```

**输出:**

```
[{ user: 'fred', active: false }, {user: 'pebbles', active: false}]

```

**例 4:**

## JavaScript

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var users = [{ 'user': 'fred',    'active': false 

},
  { 'user': 'pebbles', 'active': false }];

// Use of _.takeRightWhile() 
// method
 // The `_.property` iteratee shorthand.

let gfg =_.takeRightWhile(users, 'active');

// Printing the output 
console.log(gfg);
```

**输出:**

```
[]

```

**注意:**这段代码在正常的 JavaScript 中无法工作，因为它需要安装库 lodash。