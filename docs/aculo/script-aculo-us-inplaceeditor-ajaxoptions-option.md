# script . aculo . us in placeeditor AJaxooptions 选项

> 原文:[https://www . geesforgeks . org/script-aculo-us-in placeeditor-ajaxo options-option/](https://www.geeksforgeeks.org/script-aculo-us-inplaceeditor-ajaxoptions-option/)

**script.aculo.us** 库是一个跨浏览器库，旨在改善网站的用户界面。**阿贾克斯。InPlaceEditor** 用于使元素可编辑，从而允许用户编辑页面上的内容并将更改提交给服务器。

在定义指定给所有 AJAX 调用的选项时，使用了位置编辑器中的【AJAX 选项选项。简而言之，我们可以在编辑了就地编辑器之后，控制在提交文本期间发出的请求的类型。

**语法:**

```
{ ajaxOptions: object}
```

**值:**

*   **对象:**这是一个包含 ajax 选项的对象。

**示例:**

要演示此功能的使用，请参考以下代码。代码的 JavaScript 部分将为特定元素创建一个就地编辑器。创建一个名为“test.html”的文件，我们将使用它来发出请求。这个“test.html”将包含一个简单的文本 *GeeksforGeeks* 。点击*点击我*，你会看到原位编辑器。只需点击*确定*来提出请求，然后我们将从 Chrome 的开发工具中的网络选项卡检查请求的类型。当你点击*确定*时，它会创建一个请求，并在网络选项卡中弹出一个“test.html”，如下截图所示。

**注意:**
使用服务器运行具有 ajax 功能的文件。在本文中，我们使用的是一个 PHP 服务器。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <!-- Include the required scripts -->
    <script type="text/javascript"
        src="prototype.js"> 
    </script> 

    <script type="text/javascript"
        src="scriptaculous.js?load = effects,controls"> 
    </script> 
</head>

<body>
    <p id="editme1">Click me for post request</p>
    <p id="editme2">Click me for get request</p>

    <!-- Script for the JavaScript part to 
         initialize the objects -->
    <script type="text/javascript">
        new Ajax.InPlaceEditor('editme1', 'test.html',
         { ajaxOptions: { method: 'post' } });
        new Ajax.InPlaceEditor('editme2', 'test.html', 
        { ajaxOptions: { method: 'get' } });
    </script>
</body>

</html>
```

**发布请求输出:**

![](img/5b866fab64f340c22f244db687daab72.png)

**获取请求的输出:**

![](img/9197a8606ff35a9a8fe953a78870ef51.png)

可以看到，第一个请求方法是 POST，第二个是 GET。

**test.html**以下代码是上述 html 代码中使用的文件“test.html”的内容。

```
<!DOCTYPE html> 
<html> 

<body> 
    GeeksforGeeks
</body> 

</html> 
```