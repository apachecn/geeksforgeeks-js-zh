# 什么是 JavaScript 中的浅拷贝和深拷贝？

> 原文:[https://www . geesforgeks . org/什么是 javascript 中的浅拷贝和深拷贝/](https://www.geeksforgeeks.org/what-is-shallow-copy-and-deep-copy-in-javascript/)

JavaScript 是一种高级的、动态类型的客户端脚本语言。JavaScript 为静态 HTML 页面增加了功能。像大多数其他编程语言一样，JavaScript 允许并支持深度复制和浅复制的概念。

**浅拷贝:**当使用赋值运算符将引用变量拷贝到新的引用变量中时，将创建被引用对象的浅拷贝。简单来说，引用变量主要存储它所引用的对象的地址。当一个新的引用变量被赋予旧引用变量的值时，存储在旧引用变量中的地址被复制到新引用变量中。这意味着新旧引用变量都指向内存中的同一个对象。因此，如果对象的状态通过任何一个引用变量发生变化，它就会反映在这两个变量中。让我们举个例子来更好地理解它。

**代码实现**

## Javascript

```
var employee = {
    eid: "E102",
    ename: "Jack",
    eaddress: "New York",
    salary: 50000
}

console.log("Employee=> ", employee);
var newEmployee = employee;    // Shallow copy
console.log("New Employee=> ", newEmployee);

console.log("---------After modification----------");
newEmployee.ename = "Beck";
console.log("Employee=> ", employee);
console.log("New Employee=> ", newEmployee);
// Name of the employee as well as 
// newEmployee is changed.
```