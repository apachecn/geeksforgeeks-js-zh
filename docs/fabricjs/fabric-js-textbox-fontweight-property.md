# Fabric.js Textbox fontWeight 属性

> 原文:[https://www . geesforgeks . org/fabric-js-textbox-font weight-property/](https://www.geeksforgeeks.org/fabric-js-textbox-fontweight-property/)

在本文中，我们将看到如何使用 FabricJS 更改画布文本框的字体粗细。画布意味着所写的文本框是可移动的，可以根据需要拉伸。

**方法:**为了实现这一点，我们将使用一个名为 FabricJS 的 JavaScript 库。使用 CDN 导入库后，我们将在主体标签中创建一个画布块，其中将包含我们的文本框。之后，我们将初始化由 FabricJS 提供的 Canvas 和 Textbox 的实例，并使用 fontWeight 属性来更改字体权重，并在 Textbox 上呈现 Canvas，如下例所示。

**语法:**

```
fabric.Textbox('text', {
    fontWeight: number
});
```

**参数:**该函数接受一个参数，如上所述，如下所述:

*   **字体粗细:**指定字体粗细，可以是粗体、普通、400、500 等。

**示例:**本示例使用 FabricJS 更改画布文本框的字体粗细。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <!-- Adding the FabricJS library -->
    <script src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js">
    </script>
</head>

<body>
    <h1 style="color: green;">
        GeeksforGeeks
    </h1>

    <h3>
        Fabric.js | Textbox fontWeight Property
    </h3>

    <canvas id="canvas" width="600" height="300"
        style="border:1px solid #000000">
    </canvas>

    <script>
        // Initiate a Canvas instance 
        var canvas = new fabric.Canvas("canvas");

        // Create a new Textbox instance 
        var text = new fabric.Textbox(
            'A Computer Science Portal', {
            width: 500,
            fontWeight: 'bold'
        });

        // Render the Textbox in canvas 
        canvas.add(text);
        canvas.centerObject(text);
    </script>
</body>

</html>
```

**输出:**

![](img/d194aa4f5fa25c8c6cb054ea3e25402f.png)