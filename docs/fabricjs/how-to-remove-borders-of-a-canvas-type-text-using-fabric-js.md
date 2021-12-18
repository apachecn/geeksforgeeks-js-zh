# 如何使用 Fabric.js 移除画布类型文本的边框？

> 原文:[https://www . geesforgeks . org/如何移除画布边框-类型-文本-使用织物-js/](https://www.geeksforgeeks.org/how-to-remove-borders-of-a-canvas-type-text-using-fabric-js/)

在本文中，我们将看到如何使用 FabricJS 移除类似画布的文本的边框。画布意味着书写的文本是可移动的，可以根据需要拉伸。此外，文本本身不能像文本框一样编辑。
**方法:**为了实现这一点，我们将使用一个名为 FabricJS 的 JavaScript 库。使用 CDN 导入库后，我们将在主体标签中创建一个包含文本的*画布*块。之后，我们将初始化 FabricJS 提供的 Canvas 和 Text 的实例，并使用 **hasBorders** 属性移除边框，并在 Text 上渲染 Canvas，如下例所示。
**语法:**

```
 fabric.Text(text, hasBorders: boolean); 
```

**参数:**该功能接受两个参数，如上所述，描述如下:

*   **文本:**指定要写入的文本。
*   **有边框:**指定是启用还是禁用边框，默认启用。

**程序:**本示例使用 FabricJS 移除画布状文本的边框。请注意，您必须单击文本来查看其边框是否可见。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <title>
        How to remove borders of a canvas-type
        text with JavaScript?
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

        // Create a new Textbox instance
        var text = new fabric.Text('GeeksforGeeks', {
            hasBorders: false
        });

        // Render the Textboxes on Canvas
        canvas.add(text);
    </script>
</body>

</html>
```

**输出:**

![](img/f3868f1af9a1d3239687424a1630fd9c.png)