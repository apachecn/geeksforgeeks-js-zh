# 如何在 JavaScript 中设置高度 100%的全屏 iframe？

> 原文:[https://www . geesforgeks . org/如何设置-全屏-高度为 100 英寸的 iframe-JavaScript/](https://www.geeksforgeeks.org/how-to-set-full-screen-iframe-with-height-100-in-javascript/)

给定一个包含<iframe>元素的 HTML 文档，任务是在 JavaScript 的帮助下将<iframe>元素的高度更改为 100%。有两种方法可以改变 iframe 的高度，讨论如下:</iframe>

**方法 1:** 该方法利用带有 height 属性的 iframe 的 id 属性来改变< iframe >元素的高度。JavaScript 代码写在<脚本>标签中。

```
<html>

<head>
    <title>
        How to change the height of an
        iframe to 100% with JavaScript?
    </title>
</head>

<body style="text-align:center;">

    <h1 style="color:green;">
        GeeksforGeeks
    </h1>

    <h3>
        How to change the height of a
        <iframe id="iframe" width="100%" height="40%"
        src="https://www.youtube.com/embed/hjGD08xfg9c"
        frameborder="0" allowfullscreen>
        </iframe> to 100% with JavaScript?
    </h3>

    <br><br>

    <button onclick="changeHeight()">
        Click to change
    </button>

    <script>

        // JavaScript code to change the
        // height to 100% of <iframe>
        function changeHeight() {
            var x = document.getElementById('iframe');
            x.style.height = "100%";
        }
    </script>
</body> 

</html>
```

**输出:**

*   **点击按钮前:**
    ![](img/5b3b5977cc437147c34150a75f1ccb8b.png)
*   **点击按钮后:**
    ![](img/cda85984240325235f57e41251a17a13.png)

**方法 2:** 该方法使用带有 window.innerHeight 属性的 iframe 的 id 属性来更改< iframe >元素的高度。JavaScript 代码写在 **<脚本>** 标签内。

```
<html>

<head>
    <title>
        How to change the height of an 
        iframe to 100% with JavaScript?
    </title>
</head>

<body style="text-align:center;">

    <h1 style="color:green;">
        GeeksforGeeks
    </h1>

    <h3>
        How to change the height of a
        <iframe id="iframe" width="100%" src=
        "https://www.youtube.com/embed/hjGD08xfg9c"
        frameborder="0" ></iframe> 
        to 100% with JavaScript?
    </h3>

    <br><br>

    <button onclick="changeHeight()">
        Click to change
    </button>

    <script>

        // JavaScript code to change the
        // height to 100% of <iframe>
        function changeHeight() {
            var x = document.getElementById('iframe');
            x.style.height = window.innerHeight;
        }
    </script>
</body>

</html>
```

**输出:**

*   **点击按钮前:**
    ![](img/5b3b5977cc437147c34150a75f1ccb8b.png)
*   **点击按钮后:**
    ![](img/cda85984240325235f57e41251a17a13.png)