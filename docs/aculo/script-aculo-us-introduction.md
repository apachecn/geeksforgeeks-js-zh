# script.aculo.us 简介

> 原文:[https://www.geeksforgeeks.org/script-aculo-us-introduction/](https://www.geeksforgeeks.org/script-aculo-us-introduction/)

*script.aculo.us* 可以用来增强 GUI，给用户 Web 2.0 体验。script.aculo.us 允许我们通过文档对象模型在网络中添加动态视觉效果和用户界面。这是一个建立在原型 JavaScript 框架之上的 JavaScript 库。

**下载 script.aculo.us**

*   从 script.aculo.us [下载页面](http://script.aculo.us/downloads)下载 scriptaculous.zip 包。
*   Unzip the package and copy the following files from the *src* and *lib* folders to your website folder (here, we name the destination folder' JavaScript')
    *   建筑商。射流研究…
    *   控件。射流研究…
    *   效果。射流研究…
    *   剧本很棒。射流研究…

*   原型。射流研究…

**在你的代码中使用**

```
<!DOCTYPE html>
<html>

<head>
    <script 
        src="/javascript/prototype.js">
    </script>

    <script 
        src="/javascript/scriptaculous.js">
    </script>
</head>

<body>
    <h2>Welcome To GFG</h2>

    <p>
        Default code has been loaded 
        into the Editor.
    </p>
</body>

</html>
```

默认情况下，包含 *scriptaculous.js* 包含所有可用的效果。但是如果你想只包含一些效果，你可以用下面的代码来指定-

> <脚本 src = "/JavaScript/script aculous . js？加载=特效，拖拽“></脚本>