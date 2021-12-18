# 如何使用 Fabric.js 设置文本画布的不透明度？

> 原文:[https://www . geesforgeks . org/如何设置文本画布的不透明度-使用织物-js/](https://www.geeksforgeeks.org/how-to-set-opacity-of-a-text-canvas-using-fabric-js/)

在本文中，我们将看到如何使用 FabricJS 设置类似画布的文本的不透明度。画布意味着书写的文本是可移动、可旋转、可调整大小和可拉伸的。此外，文本本身不能像文本框一样编辑。
**方法:**为了实现这一点，我们将使用一个名为 FabricJS 的 JavaScript 库。使用 CDN 导入库后，我们将在主体标签中创建一个包含文本的*画布*块。之后，我们将初始化 FabricJS 提供的 Canvas 和 Text 的实例，并使用**不透明度**属性来设置不透明度，并在 Text 上渲染 Canvas，如下例所示。

**语法:**

```
 fabric.Text(text, opacity: number); 
```

**参数:**该函数接受两个参数，如上所述，如下所述:

*   **文本:**指定要写入的文本。
*   **不透明度:**它指定我们文本的不透明度。

**程序:**我们可以使用 FabricJS 来设置画布状文本的不透明度，使其淡化到不透明度的一半，如下所示。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <title>
        How to set the opacity of a text
        canvas using Fabric.js ?
    </title>

    <!-- Loading the FabricJS library -->
    <script src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js">
    </script>
</head>

<body>
    <canvas id="canvas" width="600" height="200"
        style="border:1px solid #000000;">
    </canvas>

    <script>

        // Create a new instance of Canvas
        var canvas = new fabric.Canvas("canvas");

        // Create a new Text instance
        var text = new fabric.Text('GeeksforGeeks', {
            opacity: 0.5
        });

        // Render the text on Canvas
        canvas.add(text);
    </script>
</body>

</html>
```

**输出:**

![](img/6c13ee4a27a83b3903b4972f9e8a732f.png)