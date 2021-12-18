# 如何使用 JavaScript 更改<textarea>的内容？</textarea>T3】

> 原文:[https://www . geesforgeks . org/如何使用 javascript 更改文本区域的内容/](https://www.geeksforgeeks.org/how-to-change-the-content-of-a-textarea-using-javascript/)

给定一个包含<textarea>元素的 HTML 文档，任务是在 JavaScript 的帮助下更改<textarea>元素的内容。</textarea>

**方法 1:** 该方法利用 textarea 的 id 属性带 value 属性来改变< textarea >元素的内容。JavaScript 代码写在 **<脚本>** 标签内。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <title>
        How to change the Content of
        a textarea using JavaScript?
    </title>
</head>

<body style="text-align:center;">

    <h1 style="color:green;">
        GeeksforGeeks
    </h1>

    <h3>
        How to change the Content of a
        <textarea> with JavaScript?
    </h3>

    <textarea id="textArea">
        A Computer Science Portal
    </textarea>

    <br><br>

    <button onclick="changeContent()">
        Click to change
    </button>

    <script>

        // JavaScript code to change
        // the content of <textarea>
        function changeContent() {
            var x = document.getElementById('textArea');
            x.value = "GeeksforGeeks";
        }
    </script>
</body>

</html>                            
```

**输出:**

*   **点击按钮前:**

![](img/e62b39d551279a04ac33322d039cbe49.png)

*   **点击按钮后:**

![](img/659e1510789a19f314108c55623dac70.png)

**方法 2:** 该方法使用带有 innerHTML 属性的 textarea 的 id 属性来更改< textarea >元素的内容。JavaScript 代码写在 **<脚本>** 标签内。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <title>
        How to change the Content of
        a textarea using JavaScript?
    </title>
</head>

<body style="text-align:center;">

    <h1 style="color:green;">
        GeeksforGeeks
    </h1>

    <h3>
        How to change the Content of a
        <textarea> with JavaScript?
    </h3>

    <textarea id="textArea">
        A Computer Science Portal
    </textarea>

    <br><br>

    <button onclick="changeContent()">
        Click to change
    </button>

    <script>

        // JavaScript code to change
        // the content of <textarea>
        function changeContent() {
            document.getElementById('textArea').innerHTML
                    = "GeeksforGeeks";
        }
    </script>
</body>

</html>                          
```

**输出:**

*   **点击按钮前:**

![](img/e62b39d551279a04ac33322d039cbe49.png)

*   **点击按钮后:**

![](img/659e1510789a19f314108c55623dac70.png)

**方法 3:** 该方法使用具有 innerText 属性的 textarea 的 id 属性来更改< textarea >元素的内容。JavaScript 代码位于 **<脚本>** 标签之间。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <title>
        How to change the Content of
        a textarea using JavaScript?
    </title>
</head>

<body style="text-align:center;">

    <h1 style="color:green;">
        GeeksforGeeks
    </h1>

    <h3>
        How to change the Content of a
        <textarea> with JavaScript?
    </h3>

    <textarea id="textArea">
        A Computer Science Portal
    </textarea>

    <br><br>

    <button onclick="changeContent()">
        Click to change
    </button>

    <script>

        // JavaScript code to change
        // the content of <textarea>
        function changeContent() {
            document.getElementById('textArea').innerText
                    = "GeeksforGeeks";
        }
    </script>
</body>

</html>                            
```

**输出:**

*   **点击按钮前:**

![](img/e62b39d551279a04ac33322d039cbe49.png)

*   **点击按钮后:**

![](img/659e1510789a19f314108c55623dac70.png)