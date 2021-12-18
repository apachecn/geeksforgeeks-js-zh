# lodash 简介

> 原文:[https://www.geeksforgeeks.org/lodash-introduction/](https://www.geeksforgeeks.org/lodash-introduction/)

**Lodash** 是一个工作在下划线. js 之上的 JavaScript 库，Lodash 有助于处理数组、字符串、对象、数字等。它为我们提供了各种内置函数，并使用了一种函数式编程方法，这种方法使得用 JavaScript 编码变得更容易理解，因为任务可以用一行代码来完成，而不是编写重复的函数。如果 javascript 中的对象需要对其进行大量的操作，那么使用 JavaScript 处理这些对象也会变得更加容易。

**安装:**可以直接使用 CDN 链接，也可以使用 npm 或纱线安装。

**方法一:**我们可以在浏览器中直接使用 Lodash 文件。转到官方文档，复制 lodash.min.js 文件 CDN 链接，并将该链接粘贴到标题部分。

**示例:**

## 超文本标记语言

```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta name="viewport" content=
        "width=device-width, initial-scale=1.0">
    <script type="text/JavaScript" src=
"https://cdn.jsdelivr.net/npm/lodash@4.17.20/lodash.min.js">
    </script>
</head>

<body>
    <script>
        console.log(_.isNumber(100));
        console.log(_.isNumber('GeeksforGeeks courses'));
        console.log(_.isNumber(78.43));
    </script>
</body>

</html>
```

**输出:**

```
true
false
true
```

**方法二:**我们可以用 npm 安装。确保您已经安装了 [Node.js](https://www.geeksforgeeks.org/installation-of-node-js-on-windows/) 和 [npm](https://www.geeksforgeeks.org/node-js-npm-node-package-manager/) 。

```
npm install lodash
```

如果您正在使用纱线，则可以使用以下命令:

```
yarn install lodash
```

现在为了使用 Lodash，您需要代码文件。

```
const _ = require("lodash");
```

现在让我们借助代码示例来理解如何使用 Lodash。

**示例:**在本例中，我们将使用 lodash [**中的内置方法之一来查找给定值参数是否为数字。**方法](https://www.geeksforgeeks.org/lodash-_-isnumber-function/)。

**index.js**

## java 描述语言

```
// Requiring the lodash library  
const _ = require("lodash");  

// Use of _.isNumber() method 
console.log(_.isNumber(100)); 
console.log(_.isNumber('GeeksforGeeks courses')); 
console.log(_.isNumber(78.43));
```

**运行程序的步骤:**用 *index.js* 保存上述文件，打开终端，输入以下命令，即可编译运行程序。

```
node index.js
```

**输出:**

```
true
false
true
```

**洛达士的优势:**

*   它为我们提供了集合、数组、操作对象和其他实用方法的各种内置函数，我们可以直接使用这些函数，而不是从头开始编写它们。
*   它使我们的代码更加简洁明了，便于以后理解和修改。
*   我们必须记住洛达什函数，这使得编码任务变得更加简单。
*   对于技术新手来说，开始和学习更容易。
*   任务可以用一行代码来完成，而不是编写重复的函数。

**洛达什的缺点:**

*   洛达什最大的缺点是速度。Lodash 方法比普通的 JavaScript 函数需要更多的时间来执行。
*   在 JavaScript 中，我们可以随心所欲地将许多函数链接在一起，但是在 Lodash 中，我们不能链接函数，我们只能包装它们。