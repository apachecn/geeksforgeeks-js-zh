# 洛达什 _。inRange()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-inrange-method/](https://www.geeksforgeeks.org/lodash-_-inrange-method/)

**_。inRange()** **方法**取一个数字，检查它是否在给定的开始和结束参数之间。如果未指定结束，则将它设置为等于开始，然后将开始设置为等于 0。如果开始值大于结束值，参数将被交换以支持负范围。

**语法:**

```
_.inRange(number, start, end)
```

**参数:**该方法接受三个参数，如上所述，如下所述:

*   **Number:** This parameter stores the number to be checked.
*   **Start:** This parameter stores the start value of the range.
*   **End:** This parameter saves the end value of the range.

**返回值:**这个方法返回**真**如果数字在范围内，否则**假**。

**例 1:**

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.inRange method 
console.log(_.inRange(12, 10)); 
console.log(_.inRange(10, 12)); 
console.log(_.inRange(5.6, 5)); 
console.log(_.inRange(5.6, 6));
```

**输出:**

```
false
true
false
true

```

**例二:**

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.inRange method 
console.log(_.inRange(2, 3, 5)); 
console.log(_.inRange(2, 2, 4)); 
console.log(_.inRange(4, 2, 4)); 
console.log(_.inRange(-2, -1, -5));
```

**输出:**

```
false
true
false
true

```