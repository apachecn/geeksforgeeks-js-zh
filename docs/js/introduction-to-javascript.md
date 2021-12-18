# JavaScript 入门

> 原文:[https://www.geeksforgeeks.org/introduction-to-javascript/](https://www.geeksforgeeks.org/introduction-to-javascript/)

**JavaScript** 是一种轻量级、跨平台、可解释的脚本语言。它以开发网页而闻名，许多非浏览器环境也使用它。JavaScript 可用于 [**客户端**](https://www.geeksforgeeks.org/server-side-client-side-programming/) 开发以及 [**服务器端**](https://www.geeksforgeeks.org/server-side-client-side-programming/) 开发。JavaScript 包含一个标准的对象库，如 [**数组**](https://www.geeksforgeeks.org/arrays-in-javascript/) 、 [**日期**](https://www.geeksforgeeks.org/javascript-date-objects/) 和 [**数学**](https://www.geeksforgeeks.org/javascript-math-object/) ，以及一组核心语言元素，如**运算符**、**控制结构**和**语句**。

![](img/785984b25214a9e5001c3949ea64c0c1.png)

*   **客户端:**它提供对象来控制浏览器及其文档对象模型。就像客户端扩展允许应用程序在 HTML 表单上放置元素并响应用户事件，如**鼠标点击**、**表单输入**和**页面导航**。对客户端有用的库有[**AngularJS**](https://www.geeksforgeeks.org/introduction-to-angularjs/)[**ReactJS**](https://www.geeksforgeeks.org/react-js-introduction-working/)**VueJS**等等。
*   **服务器端:**它提供与服务器上运行的 JavaScript 相关的对象。比如服务器端扩展允许应用程序与数据库通信，并提供从一个应用程序调用到另一个应用程序调用的信息连续性，或者在服务器上执行文件操作。最近最有名的有用框架是[T3T5。](https://www.geeksforgeeks.org/introduction-to-nodejs/)

JavaScript 可以通过[两种方式](https://www.geeksforgeeks.org/where-to-put-javascript-in-an-html-document/)添加到你的 HTML 文件中:

*   **内部 JS:** 我们可以通过在<脚本>标签内编写代码，直接将 JavaScript 添加到我们的 HTML 文件中。<脚本>标签可以根据需要放置在<头>或<体>标签内。
*   **外部 JS:** 我们可以在其他有扩展名的文件中编写 JavaScript 代码。js，然后将这个文件链接到我们想要在其中添加代码的 HTML 文件的<头>标签中。

**语法:**

```
<script>
    // JavaScript Code
</script>
```

**示例:**

## 超文本标记语言

```
<!DOCTYPE html>
<html lang="en">

<head>
    <title>
        Basic Example to Describe JavaScript
    </title>
</head>

<body>

    <!-- JavaScript code can be embedded inside
        head section or body section -->
    <script>
        console.log("Welcome to GeeksforGeeks");
    </script>
</body>

</html>
```

**输出:**输出将显示在控制台上。

```
Welcome to GeeksforGeeks
```

**JavaScript 的历史:**它由 Brendan Eich 在 1995 年创建，当时他是网景公司的工程师。它原本打算被命名为 LiveScript，但被重新命名。与大多数编程语言不同，JavaScript 语言没有输入或输出的概念。它被设计为在主机环境中作为脚本语言运行，并且由主机环境提供与外部世界通信的机制。最常见的主机环境是浏览器。
**JavaScript 的特点:**根据 **Stack Overflow** 最近进行的一项调查，JavaScript 是地球上最流行的语言。
随着浏览器技术的进步，以及 JavaScript 已经随着 Node.js 和其他框架进入服务器，JavaScript 的能力将会更强。这里有一些我们可以用 JavaScript 做的事情:

*   JavaScript 最初是为 DOM 操作而创建的。早期的网站大多是静态的，在 JS 被创建后，动态网站被创建。
*   JS 中的函数是对象。它们可能像另一个对象一样具有属性和方法。它们可以作为参数在其他函数中传递。
*   可以处理日期和时间。
*   执行表单验证，尽管表单是使用 HTML 创建的。
*   不需要编译器。

**JavaScript 的应用:**

*   **Web 开发:**给静态网站增加交互性和行为 JavaScript 是在 1995 年发明的。通过使用 AngularJS，这很容易实现。
*   **Web 应用程序:**随着技术的发展，浏览器已经进步到需要一种语言来创建健壮的 Web 应用程序的程度。当我们在谷歌地图中浏览地图时，我们只需要点击并拖动鼠标。所有详细的视图只需点击一下，这是可能的，因为只有 JavaScript。它使用为代码提供额外功能的应用程序编程接口。电子与反应在这个部门很有帮助。
*   **服务器应用:**在 Node.js 的帮助下，JavaScript 从客户端走向了服务器端，node.js 是服务器端最强大的。
*   **游戏:**不仅在网站，JavaScript 也有助于打造休闲游戏。JavaScript 和 HTML 5 的结合使得 JavaScript 在游戏开发中也很受欢迎。它提供了 EaseJS 库，该库为处理丰富的图形提供了解决方案。
*   **智能手表:** JavaScript 正在所有可能的设备和应用程序中使用。它提供了一个用于 smartwatch 应用程序的 PebbleJS 库。这个框架适用于需要互联网才能运行的应用程序。
*   **艺术:**艺术家和设计师可以使用 JavaScript 在 HTML 5 画布上绘制出自己想要的任何东西，让声音更有效果也可以使用[T3】P5 . jsT5】库。](https://www.geeksforgeeks.org/p5-js-introduction/)
*   **机器学习:**这个 JavaScript ml5.js 库可以利用机器学习用于 web 开发。

**JavaScript 的限制:**

*   **性能:** JavaScript 无法提供许多传统语言所能提供的性能水平，因为用 JavaScript 编写的复杂程序会相对较慢。但是由于 JavaScript 用于在浏览器中执行简单的任务，因此性能并不被认为是其使用的一大限制。
*   **复杂性:**要掌握一门脚本语言，程序员必须对所有的编程概念、核心语言对象、客户端和服务器端对象有透彻的了解，否则他们很难使用 JavaScript 编写高级脚本。
*   **弱错误处理和类型检查工具:**它是弱类型语言，因为不需要指定变量的数据类型。所以错误的类型检查不是通过编译来执行的。

JavaScript 最出名的是网页开发，但它也用于各种非浏览器环境。您可以通过以下 [JavaScript 教程](https://www.geeksforgeeks.org/javascript-tutorial/)和 [JavaScript 示例](https://www.geeksforgeeks.org/javascript-examples/)从头开始学习 JavaScript。