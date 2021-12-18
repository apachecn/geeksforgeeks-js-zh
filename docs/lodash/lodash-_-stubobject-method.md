# 洛达什 _。stubObject()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-stubobject-method/](https://www.geeksforgeeks.org/lodash-_-stubobject-method/)

Lodash 是一个工作在下划线. js 之上的 JavaScript 库，Lodash 有助于处理数组、字符串、对象、数字等。

**_。stubbject()**方法用于创建并返回一个空对象。

**语法:**

```
_.stubObject()

```

**参数:**此方法不接受任何参数。

**返回值:**返回一个空对象。

**例 1:**

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");            

// Using the _.stubObject() method 
// to create an empty object
let empty_obj = _.stubObject(); 

// Printing the output  
console.log(empty_obj);
```

**输出:**

```
Object {}

```

**例二:**

## Javascript

```
// Requiring the lodash library  
const _ = require("lodash");            

// Using the _.stubObject() method
// to create 5 empty Object
let empty_objs = _.times(5, _.stubObject); 

// Printing the output  
console.log(empty_objs);
```

**输出:**

```
[Object {}, Object {}, Object {}, Object {}, Object {}]

```