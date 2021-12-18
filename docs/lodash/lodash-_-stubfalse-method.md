# 洛达什 _。stubFalse()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-stubfalse-method/](https://www.geeksforgeeks.org/lodash-_-stubfalse-method/)

Lodash 是一个工作在下划线. js 之上的 JavaScript 库，Lodash 有助于处理数组、字符串、对象、数字等。

**_。stubFalse()** 方法用于始终返回一个假值。使用正常的**假的**值和使用**的基本区别。stubFalse()** 方法是 lambda 函数每次运行时都会创建一个新的不同的函数，所以在 React render 函数中使用时，可以创建不必要的重新渲染。Lodash 存根没有这个问题。

**语法:**

```
_.stubFalse()

```

**参数:**此方法不接受任何参数。

**返回值:**返回假布尔值。

**例 1:**

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");            

// Using the _.stubFalse() method 
let false_val = _.stubFalse(); 

// Printing the output  
console.log(false_val);
```

**输出:**

```
'false'
```

**例二:**

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");            

// Using the _.stubFalse() method 
// to create 5 false values
let false_vals = _.times(5, _.stubFalse); 

// Printing the output  
console.log(false_vals);
```

**输出:**

```
[false, false, false, false, false]
```