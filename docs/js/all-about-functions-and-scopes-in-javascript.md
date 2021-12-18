# 关于 JavaScript 中的函数和作用域

> 原文:[https://www . geesforgeks . org/关于函数和作用域的 javascript/](https://www.geeksforgeeks.org/all-about-functions-and-scopes-in-javascript/)

在本文中，我们将深入介绍 JS 函数、回调、作用域、闭包的所有基本概念，这将帮助您–

*   Understand different types of function declarations.
*   Make better use of functions.
*   Understand how different scopes and scope chains in JS work.
*   Learn about closures and how to use them.

我们将通过示例理解所有这些概念&也理解它们的实现。让我们从 Javascript 函数开始讨论。

**函数:** [函数](https://www.geeksforgeeks.org/functions-in-javascript/) 允许我们声明&将一堆代码打包在一个块中，这样我们就可以在程序中使用(并重用)一个代码块。有时，它们将一些值作为“参数”来执行操作，并作为操作的结果返回一些值。

**例:**

## Javascript

```
function add(a, b) {

    // a and b are the parameters of this
    // function code to do the operation
    return a + b; // return statement
}

// Invoking the function and 2, 3
// are arguments here
add(2, 3);
```

**输出:**

```
5
```

**一级公民:**如果任何编程语言能够将函数视为值，将它们作为参数传递，并从另一个函数返回函数，那么据说编程语言具有一级函数，这些函数在该编程语言中称为[一级公民](https://www.geeksforgeeks.org/what-is-first-class-citizen-in-javascript/)。如果函数:

*   Store the function in a variable, and the function will be regarded as a first-class citizen in JavaScript.
*   Pass one function as a parameter to another function.
*   Returns a function from another function.

**函数表达式:**当一个函数存储在变量中时，它被称为*函数表达式。*这个可以命名，也可以匿名。如果一个函数没有任何名字，并且存储在一个变量中，那么它将被称为*匿名函数表达式*。否则，它将被称为*命名函数表达式。*详情请参考 [JavaScript 函数表达式](https://www.geeksforgeeks.org/javascript-function-expression/)一文。

**例:**

## Javascript

```
// Anonymous function expression
const add = function (a, b){
    return a + b;
}

// Named function expression
const subtractResult = function subtract(a, b){
    return a - b;
}

console.log(add(3, 2)); // 5
console.log(subtractResult(3, 2)); // 1
```