# 洛达什 _。noop()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-noop-method/](https://www.geeksforgeeks.org/lodash-_-noop-method/)

Lodash 是一个工作在下划线之上的 JavaScript 库。Lodash 有助于处理数组、字符串、对象、数字等。

洛达什 **_。noop()** 方法用于返回“undefined”，与传递给它的参数无关。

**语法:**

```
_.noop()

```

**参数:**该方法可以取任意类型的可选参数。

**返回:**该方法返回未定义。

**例 1:**

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");              

// Use of _.noop() method 
let val = undefined; 
let val2 = _.noop(); 

if (val == val2) 
    console.log("val and val2 are equal"); 
else
    console.log(`val and val2 are not equal`);
```

**输出:**

```
val and val2 are equal

```

**例二:**

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");    

// Use of _.noop() method 
let obj = new Object(_.noop()) 
console.log(`Object is ${obj.Object}`) 

// Use of _.noop() method  
let arr = new Array(_.noop()) 
console.log(`Array is ${arr[0]}`)
```

**输出:**

```
Object is undefined
Array is undefined

```