# 洛达什 _。shuffle()方法

> 原文:[https://www.geeksforgeeks.org/lodash_-shuffle-method/](https://www.geeksforgeeks.org/lodash_-shuffle-method/)

**_。shuffle()** 方法通过返回新数组来对集合进行 shuffle。

**语法:**

```
_.shuffle(collection)

```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **Set:** This parameter stores the set to be checked.

**返回值:**此方法在洗牌后返回新数组。

**示例 1:** 这里，const _ = require('lodash ')用于导入文件中的 lodash 库。

## Javascript

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array and use _.shuffle() method
var gfg = _.shuffle([1, 2, 3,4]);

// Printing the output 
console.log(gfg);
```

**输出:**

```
[4, 1, 3, 2]

```

**例二:**

## Javascript

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array and use _.shuffle() method
var gfg = _.shuffle(["g", "e", "e", "k", "s", "f", "o",
                     "r", "g", "e", "e", "k", "s"]);

// Printing the output 
console.log(gfg);
```

**输出:**

```
["o", "e", "k", "s", "e", "e", "s",
 "g", "r", "e", "g", "f", "k"]

```

**注意:**这段代码在正常的 JavaScript 中无法工作，因为它需要安装库 lodash。