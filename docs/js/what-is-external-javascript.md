# 什么是外部 JavaScript？

> 原文:[https://www.geeksforgeeks.org/what-is-external-javascript/](https://www.geeksforgeeks.org/what-is-external-javascript/)

**JavaScript** 是最流行的*解释*、*轻量级*、*编译*的编程语言之一。它是同步和单线程的。JavaScript 中的程序被称为脚本，以纯文本形式执行。我们可以直接在我们的 HTML 页面上编写这些脚本，或者使用外部的 JavaScript 文件。JavaScript 可以在浏览器中执行，也可以在服务器上执行，或者实际上在任何具有名为 *JavaScript 引擎*的特殊程序的设备上执行。JavaScript 用于服务器端和客户端开发。

有两种方法可以在 HTML 文件中使用 javascript:

*   **内部 JavaScript** :通过在<脚本>标签里面写代码，可以将 JavaScript 直接添加到 HTML 文件中。我们可以根据需要将<脚本>标签放置在<头部>或<身体>标签内。
*   **外部 JavaScript** :另一种方法是在另一个扩展名为. js 的文件中编写 JavaScript 代码，然后将该文件链接到我们想要在其中添加该代码的 HTML 文件的<头>或<体>标签内。

**示例:**这个示例描述了内部 Javascript 的使用。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <title>Internal JS</title>
</head>

<body>
    <h2>GeeksforGeeks</h2>
    <script>

    /*Internal Javascript*/    
    console.log("Hi Geeks, Welcome to GfG");
    </script>
</body>

</html>
```

**输出**:

```
Hi Geeks, Welcome to GfG
```

**示例:**这个示例描述了外部 Javascript 的使用。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <title>External JS</title>
</head>

<body>
    <h2>GeeksforGeeks</h2> 

    <script src="GfG.js"></script> /* External Javascript */
</body>

</html>
```

**外部文件** : GfG.js

## java 描述语言

```
console.log("Hi Geeks, Welcome to GfG");
```

**输出**:

```
Hi Geeks, Welcome to GfG
```

**什么是外部 JavaScript？**

**外部 JavaScript** 是将 *JavaScript* 代码(脚本)写在另一个扩展名为的文件中。js 然后我们把这个文件链接到我们的 *HTML* 文件的<头>或者<体>标签里面，代码要添加到这个文件里面。当在许多不同的网页中使用相同的代码时，使用外部 JavaScript 更加实用。使用外部脚本很容易，只需将脚本文件的名称(我们的。js 文件)在<脚本>标签的 src (source)属性中。外部 **JavaScript** 文件不能包含<脚本>标签。

**语法:**

```
<script type="media_type" src="URL"> </script>
```

**属性值:**

*   [**类型**](https://www.geeksforgeeks.org/html-script-type-attribute/)**:**用于指定脚本的 MIME 类型，识别 Tag 的内容。它有一个默认值，即“ **”文本/JavaScript“**”。
*   [**src**](https://www.geeksforgeeks.org/html-script-src-attribute/)**:用于指定**一个外部 JavaScript 文件的 URL。
*   [**异步**](https://www.geeksforgeeks.org/html-script-async-attribute/) **:它是一个布尔属性。如果存在，它指定脚本在可用时异步执行。**
*   [**延期**](https://www.geeksforgeeks.org/html-script-defer-attribute/) :是布尔属性用于指定页面解析完毕后执行脚本。
*   [**【完整性】**](https://www.geeksforgeeks.org/html-script-integrity-attribute/)**:**用于允许浏览器检查提取的脚本，以确保源代码永远不会被加载。
*   [**【referrer policy】**](https://www.geeksforgeeks.org/html-script-referrerpolicy-attribute/)**:**It**用于指定获取脚本时会发送到服务器的引用信息。**

***多个脚本文件*也可以使用多个<脚本>标签添加到*一个*页面。**

```
<script src="file1.js"> </script>
<script src="file2.js"> >/script>
```

****示例**:本示例描述了外部 javascript 文件的使用，其中指针悬停在特定文本上，然后文本转换为不同的文本。**

## **超文本标记语言**

```
<!DOCTYPE html>
<html>

<head>
    <title>External JavaScript</title>
    <style>
    h2 {
        box-sizing: border-box;
        width: 250px;
        height: 150px;
        background-color: green;
        color: white;
        margin: auto;
        font-size: 15px;
        font-family: sans-serif;
        text-align: center;
        padding: 20px;
    }
    </style>
</head>

<body>
    <h2 class="external">GeeksforGeeks</h2>
    <script src="GfG.js"></script>
</body>

</html>
```

****JS 代码:****

## **GfG.js(联署材料)**

```
let h2 = document.querySelector(".external");
h2.addEventListener("mouseenter", function (e) {
  h2.innerText = "Hi Geeks, Welcome to GfG";
});
```

****输出**:当指针悬停在元素上时，元素内的文字(即 GeeksforGeeks)变为“嗨 Geeks，欢迎来到 GfG”。**

**![](img/1c224138ee968ea91b77ddf2e7fc7289.png)**

****使用内部 JS 的优势:****

*   **浏览器不需要对 JavaScript 代码进行额外的 HTTP 请求。**
*   **它不允许缓存。**

****内部 JS 的缺点:****

*   **代码的可读性变差。**
*   **当有大量代码时，代码的维护变得困难。**

****使用外部 JS 的优势:****

*   **HTML 和 JavaScript 文件变得更加易读和易于维护。**
*   **由于缓存的 JavaScript 文件，页面加载速度加快。**

****外部 JS 的缺点:****

*   **程序员可以使用脚本的 *url* 轻松下载您的代码。js)文件。**
*   **浏览器发出额外的HTTP 请求来获取这个 JavaScript 代码。**