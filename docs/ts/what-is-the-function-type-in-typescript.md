# TypeScript 中的函数类型是什么？

> 原文:[https://www . geesforgeks . org/什么是函数类型脚本/](https://www.geeksforgeeks.org/what-is-the-function-type-in-typescript/)

TypeScript 是一种基于 JavaScript 的编程语言，具有类型化语法。它提供了各种改进的工具。它为 JavaScript 增加了额外的语法。这有助于促进你和编辑之间更强的互动。这也有助于提前发现错误。

它使用类型推理来提供强大的工具，而不需要额外的代码。TypeScript 可以在任何支持 JavaScript 的地方执行，因为它可以转换为 JavaScript 代码。

**类型脚本函数:**函数是 JavaScript 最关键的方面，因为它是一种函数式编程语言。函数是执行指定任务的代码片段。它们用于实现面向对象的编程原则，如类、对象、多态性和抽象。用于保证程序的可重用性和可维护性。虽然 TypeScript 有类和模块的概念，但函数仍然是语言的一个重要方面。

**函数声明:**函数的名称、参数和返回类型都在函数声明中指定。函数声明如下:

**语法:**

```
function functionName(arg1, arg2, ... , argN);
```

**功能定义:**包括将要执行的实际语句。它概述了应该做什么以及如何做。函数定义如下

**语法:**

```
function functionName(arg1, arg2, ... , argN){
// Actual code for execution
}
```

**函数调用:**可以从应用程序的任何地方调用函数。在函数调用和函数定义中，参数/参数必须相同。我们必须传递函数定义指定的相同数量的参数。该函数调用具有以下内容

**语法:**

```
functionName(arg1, arg2, ... , argM);
```

**类型脚本中的函数类型:**类型脚本中有两种类型的函数:

*   命名函数
*   匿名函数

**1。命名函数:**命名函数定义为通过其给定名称声明和调用的函数。它们可能包含参数并具有返回类型。

**语法:**

```
functionName( [args] ) { }  
```

**示例:**

## java 描述语言

```
// Named Function Definition  
function myFunction(x: number, y: number): number {
  return x + y;
}

// Function Call  
myFunction(7, 5);  
```

**输出:**

```
12
```

**2。匿名函数:**匿名函数是没有名字的函数。在运行时，这些类型的函数被动态定义为表达式。我们可以将它保存在一个变量中，并消除对函数名的要求。它们接受输入和返回输出的方式与普通函数相同。我们可以在需要的时候使用变量名来调用它。函数本身包含在变量中。

**语法:**

```
let result = function( [args] ) { }  
```

**示例:**

## java 描述语言

```
// Anonymous Function  
let myFunction = function (a: number, b: number) : number {  
    return a + b;  
};  

// Anonymous Function Call  
console.log(myFuction(7, 5));
```

**输出:**

```
12
```

**功能优势:**功能优势可能包括但不限于以下内容:

*   **代码可重用性:**我们可以多次调用一个函数，而不必重写同一个代码块。代码的可重用性节省了时间并减小了程序的大小。
*   **少编码:**我们的软件因为功能比较简洁。因此，我们不需要在每次执行例行活动时都编写大量的代码行。
*   **易于调试:**让程序员发现和隔离不正确的数据变得简单。