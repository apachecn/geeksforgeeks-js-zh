# 如何在 JavaScript 中创建一个调用带有前置参数的 partials 函数的函数？

> 原文:[https://www . geeksforgeeks . org/如何创建一个调用带有部分前置参数的函数的函数/](https://www.geeksforgeeks.org/how-to-create-a-function-that-invokes-function-with-partials-prepended-arguments-in-javascript/)

在本文中，我们将看到如何创建一个函数，该函数调用在 JavaScript 中接收的参数前附加了部分的函数。在理解问题陈述和解决问题之前，让我们首先了解什么是函数(也称为方法)以及函数是如何执行的。

函数(或方法)是执行特定任务的代码块，函数就是为该任务而产生的。一个函数可以在程序中被调用任意次数来执行特定的任务。将大代码分成小代码块不仅增加了代码的可读性，而且有助于开发人员在代码的特定部分找到错误。这使得这个程序既干净又真实。基本上，对于一个特定的任务执行不止一次，我们可以在一个单独的函数(方法)中编写我们的逻辑部分，并且可以在程序中随时使用该函数。

我们有很多方法可以创建一个简单的函数(方法)，比如使用 function 关键字或者创建 arrow 函数，这两种情况下的语法会有一点不同，但是最终结果会保持不变。以下是我们可以声明我们的函数(方法)并进一步执行它的语法-

## 【Javascript】

```
function displayName (name) {
    return name;
}
console.log(displayName("GeeksforGeeks"));
```