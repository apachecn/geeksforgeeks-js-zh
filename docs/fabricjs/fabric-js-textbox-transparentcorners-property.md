# Fabric.js Textbox 透明角落属性

> 原文:[https://www . geesforgeks . org/fabric-js-textbox-transparentcorners-property/](https://www.geeksforgeeks.org/fabric-js-textbox-transparentcorners-property/)

在本文中，我们将看到如何使用 FabricJS 的 transparentCorners 属性来设置画布文本框的角的可见性。画布意味着文本框是可移动的，可以根据需要进行拉伸。此外，文本框可以自定义初始笔画颜色、填充颜色、笔画宽度或半径。

为了实现这一点，我们将使用一个名为 FabricJS 的 JavaScript 库。使用 CDN 导入库后，我们将在主体标签中创建一个画布块，其中将包含我们的文本框。之后，我们将初始化由 FabricJS 提供的 Canvas 和 Textbox 的实例，并分别使用 transparentCorners 属性设置 Textbox 的角的可见性，并在 Canvas 上呈现 Textbox，如下例所示。

**语法:**

```
fabric.Textbox('text', {
    transparentCorners: boolean
});
```

**参数:**该函数接受一个参数，如上所述，如下所述:

*   **透明角:**是一个布尔值，指定是否使控制角可见。

**示例 1:** 本示例使用 FabricJS 将画布文本框的角的可见性设置为 false。

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
        Fabric.js | Textbox transparentCorners Property
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
            strokeWidth: 3,
            cornerColor: 'cyan',
            cornerStrokeColor: 'red',
            transparentCorners: false
        });

        // Render the Textbox in canvas 
        canvas.add(text);
        canvas.centerObject(text);
    </script>
</body>

</html>
```

**输出:**

![](img/b3284405cdd99e2d6575afd68701085c.png)

**示例 2:** 本示例使用 FabricJS 将画布文本框的角的可见性设置为 true，因此控制角是透明的。

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
        Fabric.js | Textbox transparentCorners Property
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
            strokeWidth: 3,
            cornerColor: 'cyan',
            cornerStrokeColor: 'red',
            transparentCorners: true
        });

        // Render the Textbox in canvas 
        canvas.add(text);
        canvas.centerObject(text);
    </script>
</body>

</html>
```

**输出:**

![](img/359f18e0172a69676385d48b3eb44c30.png)