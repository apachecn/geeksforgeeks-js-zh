# 洛达什 _。更换()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-replace-method/](https://www.geeksforgeeks.org/lodash-_-replace-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、集合、字符串、lang、函数、对象、数字等。

**_。替换()方法**用替换替换字符串中模式的匹配。此方法基于字符串#replace。

**语法:**

```
_.replace(string, pattern, replacement)
```

**参数:**该方法接受三个参数，如上所述，如下所述:

*   **字符串:**此参数保存原始字符串。
*   **模式:**此参数保存需要替换的模式字符串。
*   **替换:**此参数保存替换字符串。

**返回值:**该方法返回修改后的字符串。

**示例 1:** 这里，const _ = require('lodash ')用于导入文件中的 lodash 库。

## JavaScript

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var string = _.replace('Stay In', 'In', 'Safe');    

// Using the _.replace() method
let replace_elem = _.replace(string);

// Printing the output 
console.log(replace_elem);
```

**输出:**

```
Stay Safe
```

**例二:**

## JavaScript

```
// Requiring the lodash library 
const _ = require("lodash"); 

// Original array 
var num = _.replace('234 56 41', '56 41', '78');     

// Using the _.replace() method
let replace_elem = _.replace(num);

// Printing the output 
console.log(replace_elem);
```

**输出:**

```
234 78
```

**注意:**这段代码在正常的 JavaScript 中无法工作，因为它需要安装库 lodash。