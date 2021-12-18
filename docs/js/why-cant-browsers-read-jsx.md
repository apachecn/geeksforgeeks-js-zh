# 为什么浏览器看不懂 JSX？

> 原文:[https://www.geeksforgeeks.org/why-cant-browsers-read-jsx/](https://www.geeksforgeeks.org/why-cant-browsers-read-jsx/)

React 是一个 JavaScript 库，用于创建网络应用程序。 **React 使用**[**【JSX】**](https://www.geeksforgeeks.org/reactjs-introduction-jsx/)**允许我们在 HTML 元素**内部编写 JavaScript 对象。JSX 既不是字符串，也不是 HTML。它是 JavaScript 的语法扩展。JSX 让代码变得简单易懂。

```
const num = 20 + 30;
const ele = <h1>{num} is 50</h1>;
```

JSX 不是一个有效的 JavaScript，因为它们嵌入在 HTML 元素中。由于 JSX 是 HTML 和 JavaScript 的结合体，所以浏览器不支持它。因此，如果任何文件包含 JSX 文件，巴贝尔 transpiler 会将 JSX 转换为 JavaScript 对象，从而成为有效的 JavaScript。因此，浏览器理解代码并执行。浏览器不能阅读 JSX，因为浏览器引擎没有内在的实现来阅读和理解它们。JSX 不打算由引擎或浏览器来实现，它打算由各种 transpilers 用来将这些 JSX 转换成有效的 JavaScript 代码。

让我们看看浏览器是如何运行 JSX 的，以及它是如何转换成 JavaScript 的。为了运行 JSX，创建一个 react 应用程序。

**创建反应应用程序:**

**步骤 1:** 使用以下命令创建一个 react 应用程序。

```
npx create-react-app foldername
```

**步骤 2:** 使用以下命令将您的目录更改为新创建的文件夹。

```
cd foldername
```

**项目结构:**创建项目结构，如下图所示；

![](img/7bb579755ddb6e1436b2f0e141251c9b.png)

项目结构

**第三步:**现在，打开 **index.js** 并添加以下代码。这个代码是在 JSX 写的。

## index.js

```
import React from 'react';
import ReactDOM from 'react-dom';

const ele = ( 
    <div className = 'page'
    style = {
        { textAlign: 'center' }
    }>
    <h1 id = 'head'> Never Stop Learning!!! </h1>
     <h2 style = {
        { color: 'green' }
    }> Because life never stops teaching </h2> 
    <p> From GeeksforGeeks </p>

    </div>
);

ReactDOM.render(ele, document.getElementById('root'));
```

**说明:**上面的代码使用巴贝尔编译器转换成了如下所示的 JavaScript，因为浏览器不支持 JSX，所以它将 JSX 代码转换成了 JavaScript。

**步骤 4:** 下面显示的代码是 JSX 的转换代码，即 JavaScript 代码(没有 JSX)。在 **index.js** 中添加以下代码，看看它是如何工作的。

## index.js

```
import React from 'react';
import ReactDOM from 'react-dom';

const ele = React.createElement("div", {
        className: 'page',
        style: { textAlign: 'center' }
    },
    React.createElement("h1", { id: 'head' }, "Never Stop Learning!!!"),
    React.createElement("h2", { style: { color: 'green' } }, 
                        "Because life never stops teaching"),
    React.createElement('p', null, "From GeeksforGeeks")
);

ReactDOM.render(ele, document.getElementById('root'));
```

**运行应用程序的步骤:**打开终端，键入以下命令。

> npm 启动

**输出:**两个代码给出相同的输出。因为它们是在 JSX 写的相同代码，另一个是转换后的 JavaScript。

![](img/b5d5cab82b7b4f5756c227c1478f09d6.png)