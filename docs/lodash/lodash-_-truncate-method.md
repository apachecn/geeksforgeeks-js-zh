# 洛达什 _。截断()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-truncate-method/](https://www.geeksforgeeks.org/lodash-_-truncate-method/)

**Lodash** 是一个工作在下划线. js 之上的 JavaScript 库，Lodash 有助于处理数组、字符串、对象、数字等。

**_。*洛达什*中字符串的截断()方法**用于在所述字符串长于指定字符串长度时将其截断。被截断的字符串的最后一个字符被所述的*省略*字符串替换，该字符串默认为“…”。

**语法:**

```
_.truncate([string=''], [options={}])

```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **【字符串= 】:**是要截断的字符串。
*   **【选项= { }】:**是选项对象。

这里的选项字段如下:

1.  **[Option. Length]:** defaults to the maximum string length *30* .
2.  **[option. ellipsis = '..']:** is a character string indicating that the text is omitted.
3.  **选项。分隔符】(正则表达式|字符串):**是要截断的分隔符模式。

**返回值:**这个方法返回截断的字符串。

**例 1:**

## Javascript

```
// Requiring lodash library
const _ = require('lodash');

// Calling _.truncate() method with 
// its parameter
let res = _.truncate(
  'GeeksforGeeks is a computer science portal.');

// Displays output
console.log(res);
```

**输出:**

```
GeeksforGeeks is a computer...
```

这里，所述字符串比字符串的最大长度长，因此其被截断，并且要在输出中返回的被截断的字符串的长度必须为 *30* ，包括*省略*字符串。

**例二:**

## Javascript

```
// Requiring lodash library
const _ = require('lodash');

// Calling _.truncate() method with 
// its parameter
let res = _.truncate(
  'GeeksforGeeks, is a computer science portal.', {
     'length': 22,
     'omission': '***'
   }
);

// Displays output
console.log(res);
```

**输出:**

```
GeeksforGeeks, is a***
```

这里，指定了字符串的最大长度以及*省略*字符串。因此，结果输出根据这个返回。