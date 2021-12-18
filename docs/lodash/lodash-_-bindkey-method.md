# 洛达什 _。bindKey()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-bindkey-method/](https://www.geeksforgeeks.org/lodash-_-bindkey-method/)

**Lodash** 是一个工作在下划线. js 之上的 JavaScript 库，Lodash 有助于处理数组、字符串、对象、数字等。

**_。 *lodash* 中的函数的 bindKey()** **方法**用于创建一个函数，该函数在*对象【key】*上调用该方法，并向它接受的参数添加分音。

**注:**

*   这个方法不同于 _。bind()方法，因为它允许绑定函数提及可能被重新解释或不存在的方法。
*   单片构建中默认为( **_** )的 *_.bindKey.placeholder* 值，用作部分使用的参数的占位符。

**语法:**

```
_.bindKey( object, key, partials )

```

**参数:**该方法接受三个参数，如上所述，如下所述:

*   **对象:**是用来调用上的方法的对象。
*   **键:**是方法中要用到的键。
*   **分句:**部分适用的是论点。这是一个可选参数。

**返回值:**该方法返回新的边界函数。

**例 1:**

## java 描述语言

```
// Requiring lodash library
const _ = require('lodash');

// Defining object parameter of this method
var obj = {
  'author': 'Nidhi',
  'welcome': function(greet, mark) {
    return greet + ' ' + this.author + mark;
  }
};

// Using the _.bindKey() method 
// with its parameters
var bound_fun =
  _.bindKey(obj, 'welcome', 'Hello');

// Calling bound_fun by passing its value
bound_fun('!!');
```

**输出:**

```
Hello Nidhi!!

```

**示例 2:** 使用带有占位符的绑定。

## java 描述语言

```
// Requiring lodash library
const _ = require('lodash');

// Defining object parameter of this method
var obj = {
  'portal': function(portal, mark) {
    return 'Welcome to ' + portal + mark;
  }
};

// Using the _.bindKey() method with its
// parameters and a placeholder
var bound_fun =
  _.bindKey(obj, 'portal', _, '!');

// Calling bound_fun by passing its value
bound_fun('GeeksforGeeks');
```

**输出:**

```
Welcome to GeeksforGeeks!

```