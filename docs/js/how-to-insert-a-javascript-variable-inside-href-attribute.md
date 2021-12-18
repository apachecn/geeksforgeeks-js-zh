# 如何在 href 属性内部插入一个 JavaScript 变量？

> 原文:[https://www . geesforgeks . org/how-insert-a-JavaScript-variable-inside-href-attribute/](https://www.geeksforgeeks.org/how-to-insert-a-javascript-variable-inside-href-attribute/)

**[<a>…</a>](https://www.geeksforgeeks.org/)**标签用于在 HTML 中创建超链接。
标签的属性之一是**href**

**href:** 指定链接指向的页面的 URL

**示例:**

```
<a href="https://www.geeksforgeeks.org/">
    GeeksforGeeks
</a>

```

**在这个*中使用变量的方法*属性:**

*   **Using onclick property:**
    This method uses the ‘onclick’ property of ‘a’ tag,
    i.e, whenever the link (‘a’ tag) is clicked, an ‘onclick’ event is triggered.
    Here we will use this onclick event to generate a new URL and redirect the user to that URL.
    (NOTE: This URL will contain the Variable we want to use inside href attribute)

    **步骤:**
    首先，我们需要了解以下术语，

    *   " location.href" ->是当前页面的整个 URL。
    *   “this”->指的是已经被点击的‘a’标签。
    *   " this.href" ->从' a '标记中获取 href 值。

    一旦我们有了“this.href”，将变量附加到它上面(这里我们使用了一个名为“XYZ”的变量)。
    然后我们需要将值附加到 URL。
    现在我们的网址已经准备好了变量及其附加值。

    在下面的例子中，我们将添加一个名为“XYZ”的变量，其值为 55。

    ```
    <!DOCTYPE html>
    <html>
    <head>
        <title>GeeksforGeeks</title>
        <script>
            var val = 55;
        </script>
    </head>
        <body>                 

            Link to <a href="https://www.google.com/"
    onclick="location.href=this.href+'?xyz='+val;return false;">
         Google
    </a>

        </body>
    </html>
    ```

    ```
    Resultant Url: https://www.google.com/?xyz=55

    ```

    “val”是一个 javascript 变量，它存储了我们想要传递给 URL 的值。
    URL 有一个名为“XYZ”的变量，该变量从 javascript 变量“val”中取值= 55。

*   **Using document.write:**
    document: When an HTML document is loaded into a web browser, it becomes a document object.
    This document object has several functions, one of them is written ().
    write(): Writes HTML expressions or JavaScript code to a document
    In this method, we will use this write() function to create an “a tag”.

    ```
    <!DOCTYPE html>
    <html>
    <head>
        <title>GeeksforGeeks</title>
        <script>
            var val = 55;
        </script>
    </head>
        <body>                 
            Link to 
            <script>
                var loc = "https://www.google.com/?xyz="+val;
                document.write('<a href="' + loc + '">Google</a>');
            </script>
        </body>
    </html>
    ```

    ```
    Resultant Url: https://www.google.com/?xyz=55

    ```

    “val”是一个 javascript 变量，它存储了我们想要传递给 URL 的值。
    URL 有一个名为“XYZ”的变量，该变量从 javascript 变量 val 中取值= 55。