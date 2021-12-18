# JavaScript 课程|理解 JavaScript 中的代码结构

> 原文:[https://www . geesforgeks . org/JavaScript-课程-理解-代码-javascript 中的结构/](https://www.geeksforgeeks.org/javascript-course-understanding-code-structure-in-javascript/)

**上一篇文章:** [JavaScript 课程|用 JavaScript 打印 Hello World](https://www.geeksforgeeks.org/javascript-course-printing-hello-world-in-javascript/)
在网页中插入 JavaScript 很像插入任何其他 HTML 内容。HTML 中用来添加 JavaScript 的标签有<脚本>和</脚本>。由<脚本>和</脚本>标签包围的代码称为脚本博客。
“类型”属性是<脚本>标签最重要的属性。然而，它不再被使用。浏览器了解到<脚本>标签里面有 JavaScript 代码。

```
<script></script>
```

**如何编写、运行和保存代码**

**方法 1:**

*   创建 html 文件(。htm)扩展，并在“script”标记内编写 javascript 代码
*   然后简单地在浏览器中加载 HTML 文件

**方法二:**

*   创建一个单独的 javascript 文件(。js)与。js 扩展。把你的代码写进去。
*   现在使用脚本阶段将这个 js 文件与 HTML 文档链接起来，比如:

```
<script src='relative_path_to_file/file_name.js'></script>
```

*   无论是身体还是大脑。

让我们借助一个简单的 javascript 示例来理解代码结构，在这个示例中，只使用 javascript 就可以使一个块消失。
**代码结构:**

```
index.html
styles.css
script.js
```

**index.html**T2】

## 超文本标记语言

```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <script src="script.js"></script>
    <link rel="stylesheet" href="styles.css">
    <title>Button Vanisher</title>
</head>

<body>
    <a onclick="toggle('plain')">
        <div id="plain">
          How many times were you frustrated while looking out for a
          good collection of programming/algorithm/interview questions?
          What did you expect and what did you get? This portal has
          been created to provide well written, well thought and
          well-explained solutions for selected questions.
          Geeksforgeeks is the one stop solution to all
          your coding problems! Join us so that we can shape
          your future.
        </div>
    </a>
</body>

</html>
```

上面的 HTML 代码包含一个简单的 div 元素，它被包装在一个锚标签(链接)中，这样每当我们单击 div 元素时，javascript 代码就可以工作了。在“div”元素中有一些随机的文本。在脚本标签中，我们将保存为“script.js”的 javascript 文件与 HTML 文档链接起来。CSS 文件也是链接的。
T1T3】

## 钢性铸铁

```
#plain {
    border: 2px solid black;
    max-width: 200px;
    height: 300px;
    margin: 0 auto;
    display: block;
}

a {
    display: block;
}
```

上面的 CSS 代码只针对标识为“普通”的两个元素“a”和“div”。
T1T3】

## java 描述语言

```
// javascript function to change the content of the

function toggle(id) {
    let button = document.getElementById(id);
    if (button.style.display == 'block') {
        button.style.display = 'none';
    } else {
        button.style.display = 'block';
    }
}
```