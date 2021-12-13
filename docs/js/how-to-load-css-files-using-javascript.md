# 如何用 JavaScript 加载 CSS 文件？

> 原文:[https://www . geesforgeks . org/如何加载 css 文件-使用-javascript/](https://www.geeksforgeeks.org/how-to-load-css-files-using-javascript/)

CSS 文件用于描述如何显示 HTML 元素。在 HTML 文档中添加 CSS 文件有多种方法。JavaScript 也可以用来在 HTML 文档中加载一个 CSS 文件。

**进场:**

*   使用 document.getElementsByTagName()方法获取 HTML 头部元素。
*   使用 createElement('link ')方法创建新的链接元素。
*   初始化链接元素的属性。
*   将链接元素附加到头部。

**示例 1:** 本示例使用 JavaScript 在 HTML 文档中添加 CSS 文件。

*   **使用名称样式创建 CSS 文件. css:**

    ```html
    .GFG {
        color:green;
    }
    ```

*   **使用 JavaScript 添加 CSS 文件:**

    ```html
    <!DOCTYPE html>
    <html>

    <head>
        <title>
            Load CSS file using JavaScript
        </title>

        <script>

            // Get HTML head element
            var head = document.getElementsByTagName('HEAD')[0]; 

            // Create new link Element
            var link = document.createElement('link');

            // set the attributes for link element 
            link.rel = 'stylesheet'; 

            link.type = 'text/css';

            link.href = 'style.css'; 

            // Append link element to HTML head
            head.appendChild(link); 
        </script> 
    </head>

    <body>
        <h2 class="GFG">GeeksForGeeks</h2>
    </body>

    </html>                    
    ```

**输出:**
![](img/af722dc4aa828bffb89f14a8254f2f9a.png)

**示例 2:** 本示例使用 JavaScript 在 HTML 文档中添加 CSS 文件。

*   **使用名称样式创建 CSS 文件. css:**

    ```html
    .GFG {
        font-size:24px;
        font-weight:bold;
        color:white;
        background-color:green;
        padding:10px;
        text-align:center;
    }
    ```

*   **使用 JavaScript 添加 CSS 文件:**

    ```html
    <!DOCTYPE html>
    <html>

    <head>
        <title>
            Load CSS file using JavaScript
        </title>

        <script>

            // Create new link Element
            var link = document.createElement('link'); 

            // set the attributes for link element
               link.rel = 'stylesheet'; 

            link.type = 'text/css';

            link.href = 'style.css'; 

            // Get HTML head element to append 
            // link element to it 
            document.getElementsByTagName('HEAD')[0].appendChild(link); 

        </script> 
    </head>

    <body>
        <div class="GFG">GeeksforGeeks</div>
    </body>

    </html>                    
    ```

**输出:**
![](img/d0956105c03897671920891a5b648b69.png)

HTML 是网页的基础，通过构建网站和网络应用程序用于网页开发。您可以通过以下 [HTML 教程](https://www.geeksforgeeks.org/html-tutorials/)和 [HTML 示例](https://www.geeksforgeeks.org/html-examples/)从头开始学习 HTML。

CSS 是网页的基础，通过设计网站和网络应用程序用于网页开发。你可以通过以下 [CSS 教程](https://www.geeksforgeeks.org/css-tutorials/)和 [CSS 示例](https://www.geeksforgeeks.org/css-examples/)从头开始学习 CSS。