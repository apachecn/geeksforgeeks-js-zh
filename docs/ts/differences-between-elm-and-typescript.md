# ELM 和 Typescript 的区别

> 原文:[https://www . geesforgeks . org/elm 和 typescript 之间的差异/](https://www.geeksforgeeks.org/differences-between-elm-and-typescript/)

**ELM:** Elm 是一种纯粹基于功能域的编程语言，用于前端 web 开发。它的语法与我们在其他编码语言中所做的不同。没有循环，有很多箭头和三角形。说到应该先学哪种编程语言，Elm 排名第 15，TypeScript 排名第 16。Elm 语言保证没有运行时错误，这使它从其他编码语言中脱颖而出。Elm 是一种强类型的基于网络的语言。在 Elm 中，不创建变量，只创建模型。Elm 自动将它们存储在内存中。Elm 更多的是功能开发。然而，人们在学习它时确实会陷入困境，并最终因为它独特的架构而放弃，但是一旦你了解了它，你就会开始享受它。

由于 JavaScript 很难维护，我们必须重构它，并且存在可维护性问题，Elm 对此采取了行动。重构起来很容易，错误更少，而且比 JavaScript 更快。由于 Elm 是一种函数式编程语言，它具有纯函数(对于相似的输入，它将产生相同的输出)等特性，不变性使它更快。Elm 使用虚拟 DOM 和 diffing。区分意味着获取当前和新的虚拟 DOM 并发现差异。Elm 使用函数也很容易维护。我们编写函数，然后像乐高一样将它们组合在一起，构建一个完整的程序。

[**TypeScript:**](https://www.geeksforgeeks.org/typescript-class/) 它是一种基于 JavaScript 构建的开源编程语言，也被称为 JavaScript 超集。所有有效的 JavaScript 代码也是[类型脚本](https://www.geeksforgeeks.org/typescript-class/)代码。您可能会遇到一些错误，但是该程序仍然在 TypeScript 中运行。TypeScript 有自己的编译器，称为 TypeScript 编译器或 [**Babel**](https://www.geeksforgeeks.org/reactjs-introduction-to-babel/) ，将 TypeScript 代码转换为 JavaScript 代码。因此，Typescript 是建立在 JavaScript 之上的。TypeScript 保护程序免受小错误的影响，因为编译器会自动捕获它们并节省时间。TypeScript 的打字系统比 JavaScript 好。TypeScript 提供了一种更好的记录方式，并验证代码是否正常工作。

**ELM vs TypeScript:**

<figure class="table">T66】TypeScript 具有平均速度。

| **ELM** | **打字稿** |
| ELM is a programming language based purely on functional domain. | Typescript is an open source language. |
| There is no loop, containing a lot of arrows and triangles. | Including loops, all valid JavaScript codes are also TypeScript codes. |
| Elm language guarantees that there are no runtime errors. | Typing manuscripts may make mistakes. |
| Elm doesn't have its own compiler, but it needs JavaScript to execute in the browser. | TypeScript has its own compiler, called TypeScript compiler or Babel, which converts TypeScript code into JavaScript code. |
| There is no such thing as "any" in ELM language, so coders are forced to write appropriate and mature code. | There is no need to write complete code, because type reasoning gives power, and people don't need to write complete code. |
| Elm uses virtual DOM and differentiating. | TypeScript can use virtual DOM, but it doesn't use differentiating. |
| Elm is neither a superscript like TypeScript nor a JavaScript framework or library. | TypeScript is a superscript and easily refactored code. |
| Elm is an inferential and reactive language, which is compiled with HTML, CSS and JavaScript to form an interactive GUI front end. | We can write TypeScript code with future JavaScript features without worrying that the code will be supported in IDE, because we can turn it into a variety of JavaScript styles. |
| Elm has defeated React and Angular in speed. |
| No variables are created in Elm, only models are created, and Elm automatically stores them in memory. | TypeScript protects all empty or undefined objects. There are no unused parameters or variables that can be stored in TypeScript language. |

</figure>

Elm 和 TypeScript 各有利弊，但这取决于如何充分利用资源。