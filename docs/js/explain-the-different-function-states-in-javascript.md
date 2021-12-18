# 用 JavaScript 解释不同的函数状态

> 原文:[https://www . geesforgeks . org/解释 javascript 中的不同函数状态/](https://www.geeksforgeeks.org/explain-the-different-function-states-in-javascript/)

在 [javascript](https://www.geeksforgeeks.org/javascript-tutorial/) 中，我们可以根据具体操作的需要，用很多不同的方式创建函数。例如，有时我们需要异步函数或同步函数。在本文中，我们将讨论函数 Person( ) { }，var person = Person()，以及 var person = new Person()之间的区别。

**函数声明:**下面给出的语法是函数的声明。代码声明了一个函数语句，但是直到我们不调用它们时才执行。在这里，Person 是函数的名称。javascript 中的函数是使用这个方法声明的。

```
function Person (){}
```

**函数声明示例:**在本例中，我们将创建一个名为 with Person 的函数，并执行如下所示的一些任务。

## Javascript

```
function Person() {
    name = "Vikash";
    age = "22";
}
```