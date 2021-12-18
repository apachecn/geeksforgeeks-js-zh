# 洛达什 _。findKey()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-findkey-method/](https://www.geeksforgeeks.org/lodash-_-findkey-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、集合、字符串、lang、函数、对象、数字等。

**_。findKey()方法**类似于 _。find()方法除了它返回第一个元素的键之外，谓词为而不是元素本身返回 true。

**语法:**

```
_.findKey(object, predicate)
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **对象:**它持有检查每个元素的对象。
*   **谓词:**它保存方法每次迭代调用的函数。

**返回值:**该方法返回匹配元素的键，否则不定义。

**示例 1:** 这里，const _ = require('lodash ')用于导入文件中的 lodash 库。

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var users = {
  'meetu':  { 'salary': 36000, 'active': true },
  'teetu':  { 'salary': 40000, 'active': false },
  'seetu':  { 'salary': 10000,  'active': true }
};

// Using the _.findKey() method
let found_elem = _.findKey(users, function(o) { return 

o.salary < 40000; });

// Printing the output 
console.log(found_elem);
```

**输出:**

```
meetu
```

**例 2:**

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var users = {
  'meetu':  { 'salary': 36000, 'active': true },
  'teetu':  { 'salary': 40000, 'active': false },
  'seetu':  { 'salary': 10000,  'active': true }
};

// Using the _.findKey() method
// The `_.matches` iteratee shorthand
let found_elem = _.findKey(users, { 'salary': 10000, 

'active': true });

// Printing the output 
console.log(found_elem);
```

**输出:**

```
seetu
```

**例 3:**

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var users = {
  'meetu':  { 'salary': 36000, 'active': true },
  'teetu':  { 'salary': 40000, 'active': false },
  'seetu':  { 'salary': 10000,  'active': true }
};

// Using the _.findKey() method
// The `_.matchesProperty` iteratee shorthand
let found_elem = _.findKey(users, ['active', false]);

// Printing the output 
console.log(found_elem);
```

**输出:**

```
teetu
```

**例 4:**

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var users = {
  'meetu':  { 'salary': 36000, 'active': true },
  'teetu':  { 'salary': 40000, 'active': false },
  'seetu':  { 'salary': 10000,  'active': true }
};

// Using the _.findKey() method
// The `_.property` iteratee shorthand
let found_elem = _.findKey(users, 'active');

// Printing the output 
console.log(found_elem);
```

**输出:**

```
meetu
```

**注意:**这段代码在正常的 JavaScript 中无法工作，因为它需要安装库 lodash。