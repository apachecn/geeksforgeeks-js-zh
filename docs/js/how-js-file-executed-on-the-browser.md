# 怎么。在浏览器上执行的 js 文件？

> 原文:[https://www . geesforgeks . org/how-js-file-on-browser-executed/](https://www.geeksforgeeks.org/how-js-file-executed-on-the-browser/)

在本文中，我们将学习如何使用以下多种方法在浏览器上执行. js 文件。关于 Javascript 的深入知识，请参考[服务器端和客户端编程，](https://www.geeksforgeeks.org/server-side-client-side-programming/)。

**怎么样。js 是由浏览器执行的？**

每个网络浏览器都有一个 JavaScript 引擎，它提供了一个 JavaScript 运行时环境。比如谷歌 Chrome 使用的是 **Lars Bak** 开发的 V8 JavaScript 引擎。V8 是由**铬项目为谷歌铬和铬网络浏览器开发的开源 JavaScript 引擎。**

浏览器的内置解释器搜索 **<脚本>** 标签或**。js** 文件在加载网页时与 HTML 文件链接，然后开始解释和执行。

**方法 1:使用普通<脚本>标记:**

**语法:**

```
<script> js code</script>
```

**示例**:在这种方法中，我们通过使用 **<脚本>** 标签，在 HTML 文件本身内编写了 JavaScript 代码。当 Web 项目中只需要几行 JS 代码时，通常首选这种方法。浏览器内置解释器在加载网页时，在 HTML 文件中搜索 **<脚本>** 标签，然后开始解释和执行。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<body>
    <script>
        document.querySelector("body").innerHTML
            = "<h2>Welcome to GeeksforGeeks</h2>";

        document.querySelector("body")
            .style.color = "green";
    </script>
</body>

</html>
```

**输出:**

![](img/1365c896b159002f1d476c321e59628b.png)

**方法二:使用<脚本 src =“>”带“src”参数:**

**语法:**

```
<script src="app.js"></script>
```

**参数:**

*   **JavaScript 文件的 src:** 文件路径

要了解文件路径的更多信息，请参考文件目录中的[路径名。](https://www.geeksforgeeks.org/path-name-in-file-directory/)

**示例:**下面是上一个示例中的 Javascript 代码，我们希望通过遵循不同的单独方法来执行这段代码。我们将创建一个单独的文件“ **app.js** ，并将下面的代码放在这个“**”中。js** ”文件。

```
app.js
```

现在，我们将使用下面的代码来链接“**”。js** 文件与 HTML 文件。对于这个任务，我们将使用一个 **<脚本 src = ">**标记，在这里我们将提供我们的**的文件路径。js** 文件中的 **src** 参数。这样，当我们的 HTML 文件开始在浏览器中加载时，浏览器的内置解释器会搜索 **<脚本>** 标签或**。js** 文件与 HTML 文件链接，然后开始解释和执行。

当 Web 项目中需要大量的 JavaScript 代码行时，这种方法是首选的，因此我们创建了一个单独的**。js** 文件和链接**。js** 文件到我们的 HTML 文件使用 **src** 参数的 **<脚本>** 标记。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<body>

  <!-- Importing app.js file-->
  <script src="app.js"></script>
</body>

</html>
```

**输出:**

![](img/1365c896b159002f1d476c321e59628b.png)