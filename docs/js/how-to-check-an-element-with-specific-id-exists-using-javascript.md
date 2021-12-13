# 如何用 JavaScript 检查特定标识的元素是否存在？

> 原文:[https://www . geesforgeks . org/如何使用 javascript 检查具有特定 id 的元素是否存在/](https://www.geeksforgeeks.org/how-to-check-an-element-with-specific-id-exists-using-javascript/)

给定一个包含一些元素的 HTML 文档，这些元素包含一些 id 属性。任务是使用 JavaScript(没有 JQuery)检查具有特定标识的元素是否存在。
下面讨论两种方法:

**方法 1:** 首先，我们将使用 document.getElementById()获取 Id，并将该 ID 存储到一个变量中。然后将元素(存储标识的变量)与“空”进行比较，并确定元素是否存在。

*   **例:**

    ```html
    <!DOCTYPE HTML>
    <html>

    <head>
        <title>
            How to check an element with specific
            ID exists using JavaScript?
        </title>
    </head>

    <body style="text-align:center;">

        <h1 style="color:green;">
            GeeksForGeeks
        </h1>

        <p id="GFG_UP"></p>

        <button onClick="GFG_Fun()">
            click here
        </button>

        <p id="GFG_DOWN"></p>

        <script>
            var el_up = document.getElementById('GFG_UP');
            var el_down = document.getElementById('GFG_DOWN');

            el_up.innerHTML = "Click on button to check if "
                        + "element exists using JavaScript.";

            function GFG_Fun() {
                var el = document.getElementById('GFGUP');
                if (el != null) {
                    el_down.innerHTML = "Element Exists";
                } else {
                    el_down.innerHTML = "Element Not Exists";
                }
            }
        </script>
    </body>

    </html>
    ```

*   **输出:**
    ![](img/f5204fd223c0b991fb15a8925df4b603.png)

**方法二:**首先，我们将使用 document.getElementById()获取 Id，并将该 ID 存储到一个变量中。然后在元素(存储标识的变量)上使用 [**JSON.stringify()方法**](https://www.geeksforgeeks.org/javascript-json-stringify-with-examples/) ，将元素与“空”字符串进行比较，然后识别元素是否存在。

*   **例:**

    ```html
    <!DOCTYPE HTML>
    <html>

    <head>
        <title>
            How to check an element with specific
            ID exists using JavaScript?
        </title>
    </head>

    <body style="text-align:center;">

        <h1 style="color:green;">
            GeeksForGeeks
        </h1>

        <p id="GFG_UP"></p>

        <button onClick="GFG_Fun()">
            click here
        </button>

        <p id="GFG_DOWN"></p>

        <script>
            var el_up = document.getElementById('GFG_UP');
            var el_down = document.getElementById('GFG_DOWN');
            el_up.innerHTML = "Click on button to check if "
                        + "element exists using JavaScript.";

            function GFG_Fun() {
                var el = document.getElementById('GFGUP');
                if (JSON.stringify(el) != "null") {
                    el_down.innerHTML = "Element Exists";
                } else {
                    el_down.innerHTML = "Element Not Exists";
                }
            }
        </script>
    </body>

    </html>
    ```

*   **输出:**
    ![](img/f5204fd223c0b991fb15a8925df4b603.png)