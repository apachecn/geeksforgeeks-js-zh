# 织物. js 文本框字符间距属性

> 原文:[https://www . geesforgeks . org/fabric-js-textbox-charspacing-property/](https://www.geeksforgeeks.org/fabric-js-textbox-charspacing-property/)

在本文中，我们将看到如何使用 FabricJS 更改 Textbox 画布的字符间距。画布文本框意味着所写的文本框是可移动的，可以根据需要进行拉伸。此外，文本本身不能像文本框一样编辑。

**进场:**

*   为了实现这一点，我们将使用一个名为 FabricJS 的 JavaScript 库。
*   使用 CDN 导入库后，我们将在主体标签中创建一个画布块，其中将包含我们的文本框。
*   之后，我们将初始化由 FabricJS 提供的 Canvas 和 Textbox 的实例，并使用 charSpacing 属性来更改字符之间的间距，并在 Textbox 上呈现 Canvas，如下例所示。

**语法:**

```
fabric.Textbox('text', {
   charSpacing: number
});
```

**参数:**该函数接受一个参数，如上所述，如下所述:

*   **字符间距:**指定字符之间的间距。

**示例:**

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <title>
        Fabric.js | Textbox charSpacing Property
    </title>

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
        Fabric.js | Textbox charSpacing Property
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
            charSpacing: 20
        });

        // Render the Textbox in canvas 
        canvas.add(text);
        canvas.centerObject(text);
    </script>
</body>

</html>
```

**输出:**

![](img/1e5f49ec7357021e6e28bec6ce312fc8.png)