# 如何用 JavaScript 改变点击按钮后T3】

> 原文:[https://www . geesforgeks . org/how-to-change-the-href-value-of-a-tag-on-button-use-JavaScript/](https://www.geeksforgeeks.org/how-to-change-the-href-value-of-a-tag-after-click-on-button-using-javascript/)

JavaScript 是一种高级的、解释的、动态类型的客户端脚本语言。HTML 用于创建静态网页。当与 HTML 和 CSS 一起使用时，JavaScript 支持交互式网页。文档对象操纵(DOM)是一种用于 HTML 和 XML 文档的编程接口。DOM 充当了 JavaScript 和 HTML 结合 CSS 的接口。DOM 将文档表示为节点和对象，即浏览器将每个 HTML 标记转换为我们可以操作的 JavaScript 对象。DOM 是网页的面向对象表示，可以用脚本语言(如 JavaScript)进行修改。要操作文档中的对象，我们需要选择它，然后进行操作。

可以通过五种方式选择元素:

*   **[document.querySelector()方法:](https://www.geeksforgeeks.org/html-dom-queryselector-method/)** 返回与查询匹配的第一个元素。
*   **[document . queryselectorall()方法:](https://www.geeksforgeeks.org/html-dom-queryselectorall-method/)** 返回与查询匹配的所有元素。
*   **[document.getElementById()方法:](https://www.geeksforgeeks.org/html-dom-getelementbyid-method/)** 返回与 Id 匹配的一个元素。
*   **[document . getelementsbyclassname()方法:](https://www.geeksforgeeks.org/html-dom-getelementsbyclassname-method/)** 它返回与类匹配的所有元素。
*   **[document . getelementsbytagname()方法:](https://www.geeksforgeeks.org/html-dom-getelementsbytagname-method/)** 它返回一个与标签名匹配的元素列表。

DOM 允许属性操作。属性控制 HTML 标签的行为或提供关于标签的附加信息。JavaScript 提供了几种操作 HTML 元素属性的方法。

以下方法用于操作属性:

*   **[getAttribute()方法:](https://www.geeksforgeeks.org/html-dom-getattribute-method/)** 返回元素上某个属性的当前值，如果元素上不存在指定的属性，则返回 null。
*   **[setAttribute()方法:](https://www.geeksforgeeks.org/php-domelement-setattribute-function/)** 它更新指定元素上已经存在的属性的值，否则会添加一个具有指定名称和值的新属性。
*   **[removeAttribute()方法:](https://www.geeksforgeeks.org/html-dom-removeattribute-method/)** 用于移除指定元素的一个属性。

下面的代码演示了属性操作，其中

**例 1:**

```
<!DOCTYPE html>
<html>

<head>
    <title>
        How to change the href attribute
        dynamically using JavaScript?
    </title>
</head>

<body style="text-align:center;">

    <h1 style="color:green">
        GeeksforGeeks
    </h1>

    <h3>
        Change the href attribute value<br>
        dynamically using JavaScript
    </h3>

    <a href="https://www.google.com">
        Go to Google
    </a>

    <br><br>

    <button onclick="myFunction()">
        Click Here!
    </button>

    <script type="text/javascript">
        function myFunction() { 
            var link = document.querySelector("a");
            link.getAttribute("href");
            link.setAttribute("href",
                "https://www.geeksforgeeks.org");
            link.textContent = "Go to GeeksforGeeks";
        }
    </script>
</body>

</html>
```

**输出:**
![](img/39ea246c729f1bf921748c09b4ad083b.png)

**说明:**点击按钮前链接打开 https://www.google.com。当点击按钮时，调用函数 myFunction()，该函数选择< a >标签的 href 属性并将其值更新为 https://www.geeksforgeeks.org，由于 HTML 文档中只有一个< a >标签，我们旨在更改其属性值，因此我们使用 querySelector()并使用 setAttribute()方法更新属性。

**例 2:**

```
<!DOCTYPE html>
<html>

<head>
    <title>
        How to change the href attribute
        dynamically using JavaScript?
    </title>
</head>

<body style="text-align:center;">

    <h1 style="color:green">
        GeeksforGeeks
    </h1>

    <h3>
        Change the href attribute value<br>
        dynamically using JavaScript
    </h3>

    <a href="https://www.google.com" id="myLink">
        Go to Google
    </a>

    <br><br>

    <button onclick="myFunction()">
        Click Here!
    </button>

    <script type="text/javascript">
        function myFunction() { 
            document.getElementById('myLink').href
                ="https://www.geeksforgeeks.org";

            document.getElementById("myLink")
                .textContent = "Go to GeeksforGeeks";
        }
    </script>
</body>

</html>
```

**输出:**
![](img/39ea246c729f1bf921748c09b4ad083b.png)

**说明:**点击按钮前链接打开 https://www.google.com。当点击按钮时，会调用函数 myFunction()，该函数选择< a >标签的 href 属性，并将其值更新为 https://www.geeksforgeeks.org。在这种方法中，getElementById()方法用于选择目标 URL 将被更改的元素。