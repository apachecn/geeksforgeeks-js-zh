# 当我们直接赋值变量而不用 JavaScript 声明时会发生什么？

> 原文:[https://www . geesforgeks . org/what-what-what-what-what-what-what-what-what-what-what-what-what-what-what-what-what-what-what-what-what-what-what-what-what-what-what-](https://www.geeksforgeeks.org/what-happen-when-we-directly-assign-the-variable-without-declaring-it-in-javascript/)

JavaScript 有两个作用域，分别是**局部作用域**和**全局作用域**，当我们直接赋值一个变量而不声明时，它就变成了窗口对象的**全局属性。****窗口是浏览器的对象。它不是 JavaScript 的对象。它由浏览器自动创建，可以从网页的任何地方访问。**

**让我们给变量 **x** 赋值而不声明它，借助 **hasOwnProperty()** 方法检查变量 **x** 是否属于窗口对象。**

****例 1:****

## **Javascript**

```
// Before x is not assigned
console.log(`1 -> ${window.hasOwnProperty('x')}`);

x= 2; // Assigning x without declaring it

console.log(`2 -> ${window.hasOwnProperty('x')}`); 

// To show both value refers to same object
console.log(` 3 -> ${window.x === x}`);
```