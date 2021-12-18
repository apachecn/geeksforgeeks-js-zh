# JavaScript 中哪些关键词用于处理异常？

> 原文:[https://www . geeksforgeeks . org/哪些关键字用于处理 javascript 中的异常/](https://www.geeksforgeeks.org/which-keywords-are-used-to-handle-exceptions-in-javascript/)

JavaScript 通过“尝试”来处理异常..catch…finally”语句。下面显示了一个示例语句。

```
try {
  // Attempt to execute this code
} catch (exception) {
  // This code handles exceptions
} finally {
  // This code always gets executed
}
```

“try…catch…finally”块的第一个元素是“try”子句。“try”子句用于限制可能生成异常的代码块，并且对于实现是强制性的。“尝试”条款应该伴随着“捕获”和“最后”条款中的一个或每一个。

**The“catch”block:**“try…catch…finally”的第二个元素是“catch”子句。“catch”子句是一个代码块，如果在“try”子句中发生异常，它将是最有效的。虽然“catch”条款是可选的，但是没有它处理异常是不够的。这是因为“catch”子句阻止异常通过决策堆栈传播，从而允许该系统恢复。如果在“try”块中发生异常，那么它会被立即交给“catch”子句。异常被传递到“catch”块进行处理。下面的实例展示了如何使用“catch”子句来处理“ReferenceError”。请注意，“ReferenceError”项通过“exception”变量包含在“catch”子句中。

```
try {

 // ReferenceError
  foo++;  
} catch (exception) {

  // It handles the exception
  var message = exception.message;  
}
```

复杂的程序会产生一些异常。在这种情况下，[“instance of”](https://www.geeksforgeeks.org/instanceof-operator-in-javascript/)运算符可用于区分各种异常。在这个例子中，预期“try”子句可以生成各种异常。对应的“catch”子句使用“instanceof”从所有不同类型的错误中逐一处理“TypeError”和“ReferenceError”异常。

```
try {

  // Assuming an exception is occurring
} catch (exception) {
  if (exception instanceof TypeError) {

    // This part handles TypeError exceptions
  } else if (exception instanceof ReferenceError) {

    // This part handles ReferenceError exceptions
  } else {

    // This part handles all other 
    // types of exceptions
  }
}
```

**finally 块:**try…catch…finally 语句的最后一个元素是可选的，即“finally”子句。“finally”子句是在“try”和“catch”子句之后执行的代码块，与任何错误无关。“finally”子句有利于平滑代码(剩余文件等)。请注意，即使没有捕获到异常，也会执行“finally”子句。在这种情况下，会执行“finally”子句，之后抛出的异常会正常进行。

尽管“try”或“catch”子句执行“return”声明，但“finally”子句仍将执行。例如，后续特性返回 fake，因为“finally”子句是最后执行的因素。

```
function case() {
  try {
    return true;
  } finally {
    return false;
  }
}
```

**抛出异常:** JavaScript 允许程序员使用“抛出”语句抛出他们自己的异常。通过使用它，程序员调试和跟上变得不那么困难。可以作为异常抛出的统计信息的种类没有限制。类似地，在各种各样的实例中，相同的统计数据可能会被卡住和抛出，这是没有限制的。

“throw”语句可以用于任何类型的数据，有很多好处。Firefox 给出了对象的调试信息，比如发生异常的文件中的行号。

例如，一个*除法*操作发生在文件的某个地方。*除法*会因为被零除而导致 JavaScript 中的“NaN”而导致一些问题。这可能会产生难以调试的混乱结果。如果应用程序抛出关于*除以零*的异常，事情就简单多了。下面的“if”语句通过引发异常来解释这种情况。

虽然“throw”语句可以用于任何统计数据类型，但是使用集成异常类型也有积极的好处。例如，Firefox 通过包含调试事实以及异常发生的文件名和行号的方式，为用户的小工具提供了一种独特的补救方法。

```
if (denominator === 0)
  throw new Error("Attempted division by zero!");
```