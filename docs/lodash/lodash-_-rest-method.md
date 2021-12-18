# 洛达什 _。休息()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-rest-method/](https://www.geeksforgeeks.org/lodash-_-rest-method/)

**Lodash** 是一个工作在下划线. js 之上的 JavaScript 库，Lodash 有助于处理数组、字符串、对象、数字等。

**_。rest()方法**用于创建一个函数，该函数调用给定的*函数*和所创建函数的*这个*绑定，以及从开始位置开始的一系列参数。

**语法:**

```
_.rest( func, start )

```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **功能:**它是用于将静止参数应用于的功能。
*   **开始:**是静止参数的开始位置。这是一个可选参数。

**返回值:**该方法返回新函数。

**例 1:**

## java 描述语言

```
// Requiring lodash library
const _ = require('lodash');

// Using the _.rest() method
// with its parameter
var write = _.rest(function(author, portal) {
    return author + portal;
  }, [1]);

// Calling write with its values
write(['Nidhi', 'GeeksforGeeks']);
```

**输出:**

```
Nidhi,GeeksforGeeks

```

**例 2:**

## java 描述语言

```
// Requiring lodash library
const _ = require('lodash');

// Using the _.rest() method
// with its parameter
var called = _.rest(function(who, whom) {
    return who + ' ' +
      _.initial(whom).join(', ') +
      (_.size(whom) > 2 ? ', and ' : '') +
      _.last(whom);
  });

// Calling called with values 
called('Teacher called', 'nidhi',
       'nisha', 'preeti.');
```

**输出:**

```
Teacher called nidhi, nisha, and preeti.

```