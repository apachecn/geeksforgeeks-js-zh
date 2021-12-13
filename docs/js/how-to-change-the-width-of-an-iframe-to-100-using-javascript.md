# 如何使用 JavaScript 将`iframe`的宽度改为 100%？

> 原文:[https://www . geesforgeks . org/如何使用 javascript 将 iframe 的宽度更改为 100/](https://www.geeksforgeeks.org/how-to-change-the-width-of-an-iframe-to-100-using-javascript/)

给定一个包含<iframe>元素的 HTML 文档，任务是在 JavaScript 的帮助下将<iframe>元素的宽度更改为 100%。有两种方法可以改变 iframe 的宽度，讨论如下:</iframe>

**方法 1:** 该方法利用带有 width 属性的 iframe 的 id 属性来改变< iframe >元素的宽度。JavaScript 的代码写在<脚本>标签中。

## 超文本标记语言

```html
<!DOCTYPE html>
<html> 

<head> 
    <title> 
        How to change the width of an 
        iframe to 100% with JavaScript? 
    </title> 
</head> 

<body> 
    <center>
        <h1 style="color:green;"> 
            GeeksforGeeks  
        </h1> 
        <h3> 
            How to change the width of a <br>
            to 100% with JavaScript? 
        </h3> 
        <iframe id="iframe" height="100%" width="40%"
            src="https://www.youtube.com/embed/HzeK7g8cD0Y"
            frameborder="0" allowfullscreen> 
        </iframe>

        <br><br> 
        <button onclick="changewidth()"> 
            Click to change 
        </button> 

        <script> 

            // JavaScript code to change the 
            // width to 100% of <iframe> 
            function changewidth() { 
                var x = document.getElementById('iframe'); 
                x.style.width = "100%"; 
            } 
        </script> 
    </center>
</body>  
</html>
```

**输出:**

*   **点击按钮前:**
    ![](img/7942d377919ffebdbb4d76c2287cf33e.png)*   **After clicking the button:**
    ![](img/12aeb7889cbf3aeb35785e1be5d7a7ed.png)

    **方法 2:** 该方法使用带有 window.innerWidth 属性的 iframe 的 id 属性来更改< iframe >元素的宽度。JavaScript 代码写在<脚本>标签中。

    ## 超文本标记语言

    ```html
    <!DOCTYPE html>
    <html> 

    <head> 
        <title> 
            How to change the width of an 
            iframe to 100% with JavaScript? 
        </title> 
    </head> 

    <body> 
        <center>
            <h1 style="color:green;"> 
                GeeksforGeeks  
            </h1> 
            <h3> 
                How to change the width of a <br>
                to 100% with JavaScript? 
            </h3> 
            <iframe id="iframe" height="100%" width="40%"
                src="https://www.youtube.com/embed/HzeK7g8cD0Y"
                frameborder="0" allowfullscreen> 
            </iframe>

            <br><br> 
            <button onclick="changewidth()"> 
                Click to change 
            </button> 

            <script> 
                // JavaScript code to change the 
                // width to 100% of <iframe> 
                function changewidth() { 
                    var x = document.getElementById('iframe'); 
                    x.style.width = window.innerWidth; 
                } 
            </script> 
        </center>
    </body>  
    </html>
    ```

    **输出:**

    *   **点击按钮前:**
        ![](img/95c3dcaa4c57b57f02c1572b9de6a6a2.png)
    *   **点击按钮后:**
        ![](img/c220b231d7d8ec1390cc47220195ac86.png)