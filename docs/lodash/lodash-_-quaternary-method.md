# 洛达什 _。四元()法

> 原文:[https://www.geeksforgeeks.org/lodash-_-quaternary-method/](https://www.geeksforgeeks.org/lodash-_-quaternary-method/)

洛达什 **_。第四纪()** r 返回一个新的函数，该函数只接受四个参数，并将这些参数传递给给定的函数。其他参数将被丢弃。

**语法:**

```
_.quaternary( fun )

```

**参数:**该方法采用如上所列的单个参数，讨论如下。

*   **乐趣:**这是给定的功能。

**返回值:**这个方法返回一个新的函数。

**注意:**要执行以下示例，您必须使用此命令提示符安装 **lodash-contrib** 库，并执行以下命令。

```
npm install lodash-contrib

```

**例 1:**

## java 描述语言

```
// Defining lodash contrib variable
var _ = require('lodash-contrib'); 

// Function
function fun(){
    return arguments;
}

// Making quaternary function
var gfgFunc = _.quaternary(fun);

console.log("Arguments are :", gfgFunc(
    "first", "second", "third", "fourth"));
```

**输出:**

```
Arguments are : [Arguments] {
  '0': 'first',
  '1': 'second',
  '2': 'third',
  '3': 'fourth'
}

```

**例 2:**

## java 描述语言

```
// Defining lodash contrib variable
var _ = require('lodash-contrib'); 

// Function
function fun(){
    return arguments;
}

// Making quaternary function
var gfgFunc = _.quaternary(fun);

// Rest arguments are excluded
console.log("Arguments are :", gfgFunc(
    "a", "b", "c", "d", "e", "f"));
```

**输出:**

```
Arguments are : [Arguments] 
  { '0': 'a', '1': 'b', '2': 'c', '3': 'd' }

```

**示例 3:** 在本例中，我们将添加参数，但只有前 4 个参数将使用此方法。

## java 描述语言

```
// Defining lodash contrib variable
var _ = require('lodash-contrib'); 

// Function
function add(){
    s = 0
    for(i = 0; i < 4; i++){
        s += arguments[i]
    }
    return s;
}

// Making quaternary function
var gfgFunc = _.quaternary(add);

// Rest arguments are excluded
console.log("Sum of first 4 arguments is :",
    gfgFunc(100, 100, 100, 100, 100));
```

**输出:**

```
Sum of first 4 arguments is : 400

```