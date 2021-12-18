# 如何用 JavaScript 创建可编辑 div？

> 原文:[https://www . geesforgeks . org/如何创建-可编辑-div-使用-javascript/](https://www.geeksforgeeks.org/how-to-create-editable-div-using-javascript/)

在本文中，我们将向您解释如何使用 HTML、CSS 和 JavaScript 创建一个可编辑的 div。一个可编辑的 div 是一个你可以点击的 div，然后它会生成一个可编辑的文本区域来编辑或者在你的浏览器上写任何文本。编辑后，当您点击浏览器上的其他位置时，该文本将显示为常量文本(不可编辑)。

**先决条件:**你应该熟悉 HTML、CSS 和 JavaScript 的基础知识。

**创建结构:**为 HTML 和 JavaScript 创建两个文件。要创建这些文件，运行以下命令

*   **Syntax:**

    ```
    $ touch index.html app.js
    ```

*   **Step 1:** Edit I **ndex.html** *.* This file contains the following codes.

    ## HTML

```
<!DOCTYPE html>
<html lang="en">

    <body>

        <h1 style="color: green;  
                   text-align: center;">
            Creating Editable Div GeeksforGeeks
        </h1>

        <div style="text-align: center; 
                    margin-left: 35%;" 
             class="container">
            <div id="first"></div>
        </div>

    </body>

    <script src="app.js"></script>
</html>
```