# 如何用 JavaScript 编写函数？

> 原文:[https://www . geesforgeks . org/如何编写 javascript 函数/](https://www.geeksforgeeks.org/how-to-write-a-function-in-javascript/)

**简介:**函数是可重用代码的集合，可以从应用程序的任何地方调用。这避免了反复编写相同代码的需要。它帮助程序员创建模块化代码。函数使程序员能够将一个大程序分解成几个更小、更易管理的函数。

函数是 JavaScript 的核心构建元素之一。在 JavaScript 中，一个函数相当于一个过程——一系列执行任务或计算值的单词——但是一个过程要想成为一个函数，它必须接受一些输入，并产生一个在输入和结果之间有明确联系的输出。要使用一个函数，必须在调用它的范围内的某个地方定义它。

**函数定义:** 函数定义或函数语句以 Function 关键字开始，并以下列内容继续。

*   A comma-separated list of function parameters in parentheses.
*   Enclose the statement in curly braces.

**语法:**

```
function name(arguments)
{
 javascript statements
}
```

**函数调用:** 要在脚本中稍后调用函数，只需键入函数的名称。默认情况下，所有 JavaScript 函数都可以利用参数对象。每个参数的值都存储在 arguments 对象中。arguments 对象类似于数组。它的值可以使用索引来访问，很像数组。但是，它不提供数组方法。

## Javascript

```
<script type = "text/javascript">
  function welcome() {
    console.log("welcome to GfG");
  }

  // Function calling
  welcome();
</script>
```

**输出:**

```
welcome to GFG
```

**函数参数:** 函数可以包含一个或多个由调用代码发送的参数，并且可以在函数中使用。因为 JavaScript 是一种动态类型的编程语言，所以函数参数可以有任何数据类型作为值。

## Javascript

```
<script type = "text/javascript"> 
  function welcome(name) {
    console.log("Hey "+""+name+" "+"welcome to GfG");
  }

  // Passing arguments
  welcome("Rohan");
</script>
```

**输出:**

```
Hey Rohan welcome to GFG
```

**返回值:** 返回语句是 JavaScript 函数的可选部分。如果希望从函数返回值，必须这样做。这应该是函数的最终语句。

## Javascript

```
<script type = "text/javascript">
  function welcome() {

    // Return statement
    return "Welcome to GfG";
  }

  welcome();
</script>
```