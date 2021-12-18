# 洛达什 _。快照()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-snapshot-method/](https://www.geeksforgeeks.org/lodash-_-snapshot-method/)

**Lodash** 是一个工作在下划线. js 之上的 JavaScript 库，Lodash 有助于处理数组、字符串、对象、数字等。

**_。snapshot()方法**用于对给定对象进行深度快照或克隆。

**语法:**

```
_.snapshot( obj )

```

**参数:**该方法取一个对象创建一个深度克隆。

**返回值:**此方法返回克隆的对象。

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装 lodash contrib 库。可以使用 **npm 安装 Lodash-contrib–保存**来安装 Lodash contrib 库。

**例 1:**

## java 描述语言

```
// Defining the lodash-contrib variable 
var _ = require('lodash-contrib');

// The given object
var given_object =
  { "a": 100, "b": 200, "c": 300 }; 

// Using the _.snapshot() method
// to create the deep clone
var cloned_obj = _.snapshot(given_object);

console.log("Cloned Object: ", cloned_obj);
```

**输出:**

```
Cloned Object: Object {1: "a", 2: "b"}

```

**例 2:**

## java 描述语言

```
// Defining the lodash-contrib variable 
var _ = require('lodash-contrib');

// The given array
var given_array = [5, 10, 15, 20, 25]; 

// Using the _.snapshot() method
// to create the deep clone
var cloned_arr = _.snapshot(given_array);

console.log("Cloned Array: ", cloned_arr);
```

**输出:**

```
Cloned Object: [1, 2, 3, 4]

```

**例 3:**

## java 描述语言

```
// Defining the lodash-contrib variable 
var _ = require('lodash-contrib');

// The given string
var given_string = "GeeksforGeeks"

// Using the _.snapshot() method
// to create the deep clone
var cloned_string = _.snapshot(given_string);

console.log("Cloned String: ", cloned_string);
```

**输出:**

```
Cloned Object: GeeksforGeeks

```

**例 4:**

## java 描述语言

```
// Defining the lodash-contrib variable 
var _ = require('lodash-contrib');

// The given number
var given_number = 789434;

// Using the _.snapshot() method
// to create the deep clone
var cloned_num = _.snapshot(given_number);

console.log("Cloned Number: ", cloned_num);
```

**输出:**

```
Cloned Object: 10000

```