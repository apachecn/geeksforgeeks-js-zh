# 如何在 JavaScript 中将数组推入对象？

> 原文:[https://www . geesforgeks . org/如何将数组推入 javascript 对象中/](https://www.geeksforgeeks.org/how-to-push-an-array-into-the-object-in-javascript/)

为了在 JavaScript 中将数组推入对象，我们需要利用 [push()函数](https://www.geeksforgeeks.org/javascript-array-prototype-push-function/)。借助数组推送功能，这个任务很容易实现。

[**push()函数**](https://www.geeksforgeeks.org/javascript-array-prototype-push-function/) **:** 数组 push()函数在数组末尾添加一个或多个值，并返回新长度。此方法更改数组的长度。但是这里我们将使用这个函数把整个数组推进一个对象。

**语法:**

```
arr.push(element1[, ...[, elementN]])
```

一个数组可以通过 **push()** 函数插入到对象中，下面的例子说明了上面的方法:

**例 1:**

## java 描述语言

```
<script>
// JavaScript program to add array into
// an object using push() function

// Creating a JS object to add array into it
var Obj = {             
    arrayOne: [],
    arrayTwo: []
};

// Array to be inserted
var arraynew = ['Geeks', 'for', 'Geeks'];

// Push an array to object
Obj.arrayOne.push(arraynew);     

alert(Obj.arrayOne);

</script>                     
```

**输出:**

![Output after inserting array](img/45c9468d0104f79f68d799ca32011584.png)

**例 2:**

## java 描述语言

```
<script>
// JavaScript program to add array into
// an object using push() function

// Creating a JS object to add array into
var Obj = {             
    arrayOne: ['Geeks', 'for', 'Geeks'],
    arrayTwo: []
};

// Array to be inserted
var arraynew = ['Hello', 'World', '!!!']; 

// Pushing of array into arrayTwo
Obj['arrayTwo'].push(arraynew);     

alert(Obj.arrayTwo);

</script>                    
```

**输出:**

![Output after inserting array2](img/445df071507b89b8084e4e102143c1f9.png)

**支持的浏览器:****数组推送()功能**支持的浏览器如下:

*   谷歌 Chrome 1.0
*   Internet Explorer 5.5
*   Mozilla Firefox 1.0
*   旅行队
*   歌剧

JavaScript 最出名的是网页开发，但它也用于各种非浏览器环境。您可以通过以下 [JavaScript 教程](https://www.geeksforgeeks.org/javascript-tutorial/)和 [JavaScript 示例](https://www.geeksforgeeks.org/javascript-examples/)从头开始学习 JavaScript。