# 洛达什 _。isValidDate()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-isvaliddate-method/](https://www.geeksforgeeks.org/lodash-_-isvaliddate-method/)

**Lodash** 是一个工作在下划线. js 之上的 JavaScript 库，Lodash 有助于处理数组、字符串、对象、数字等。

**_。isValidDate()方法**用于检查给定值是否为有效日期。如果该值既是日期对象的实例，并且该日期对象代表有效日期，则检查该值。

**注意:**此方法不验证原始输入的 to Date 是否为真实日期。例如，日期字符串“02/30/2014”被视为有效日期，因为 date 对象将其解释为日期表示“03/02/2014”，这是正确的。像 Moment.js 这样的库可以用来验证表示日期的字符串。

**语法:**

```
_.isValidDate( value )

```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **值:**此参数保存需要检查有效日期的值。

**返回值:**这个方法返回一个布尔值。如果给定值是有效日期，则返回 true，否则返回 false。

**注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装 lodash contrib 库。可以使用 **npm 安装 Lodash-contrib–保存**来安装 Lodash contrib 库。

**例 1:**

## java 描述语言

```
// Defining Lodash variable 
const _ = require('lodash-contrib'); 

var validDate = new Date("10/02/2014");
var invalidDate = new Date("10/32/2014");

// Checking for Valid Date Object 
console.log("The Value of Valid Date : " +
  _.isValidDate(validDate));
console.log("The Value of Invalid Date : " +
  _.isValidDate(invalidDate));
```

**输出:**

```
The Value of Valid Date : true
The Value of Invalid Date : false

```

**例 2:**

## java 描述语言

```
// Defining Lodash-contrib variable 
const _ = require('lodash-contrib'); 

var val = "World War 2"; 

// Checking for Valid Date Object 
console.log("The Value of Date : " +
  _.isValidDate(val));
```

**输出:**

```
The Value of Date : false

```