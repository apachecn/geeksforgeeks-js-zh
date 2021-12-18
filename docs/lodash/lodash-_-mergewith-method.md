# 洛达什 _。合并()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-mergewith-method/](https://www.geeksforgeeks.org/lodash-_-mergewith-method/)

Lodash 是一个工作在下划线. js 之上的 JavaScript 库，Lodash 有助于处理数组、字符串、对象、数字等。

**_。mergeWith()** 方法使用一个定制函数，调用该函数来产生给定目标和源属性的合并值。当定制函数返回*未定义时，*合并由方法处理。几乎和 _。merge()方法。

**语法:**

```
_.mergeWith( object, sources, customizer )

```

**参数:**该方法接受三个参数，如上所述，如下所述:

*   **对象:**此参数保存目标对象。
*   **来源:**此参数保存来源对象。这是一个可选参数。
*   **定制器:**这是定制赋值的功能。

**返回值:**该方法返回对象。

**例 1:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// The destination object
var object = {
  'amit': [{ 'susanta': 20 }, { 'durgam': 40 }]
};

// The source object
var other = {
  'amit': [{ 'chinmoy': 30 }, { 'kripamoy': 50 }]
};

// Using the _.mergeWith() method 
console.log(_.mergeWith(object, other));
```

**输出:**

> -30，苏珊娜，20-40，kri pke，50

**例 2:**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Defining the customizer function
function customizer(obj, src) {
  if (_.isArray(obj)) {
    return obj.concat(src);
  }
}

// The destination object
var object = {
  'amit': [{ 'susanta': 20 }, { 'durgam': 40 }]
};

// The source object
var other = {
  'amit': [{ 'chinmoy': 30 }, { 'kripamoy': 50 }]
};

// Using the _.mergeWith() method 
console.log(_.mergeWith(object, other, customizer));
```

**输出:**

> -好吧，好吧，好吧，好吧，好吧，好吧，好吧，好吧，好吧，好吧，好吧，好吧，好吧，好吧，好吧，好吧，好吧，好吧，好吧，好吧，好吧，好吧，好吧，好吧，好吧，好吧，好吧，好吧，好吧，好吧，好吧，好吧