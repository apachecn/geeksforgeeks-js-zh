# 如何使用 Fabric.js 改变文本画布的字体大小？

> 原文:[https://www . geeksforgeeks . org/如何使用织物更改文本画布的字体大小-js/](https://www.geeksforgeeks.org/how-to-change-the-font-size-of-a-text-canvas-using-fabric-js/)

在本文中，我们将看到如何使用 FabricJS 更改文本画布的字体大小。文本画布是指书写的文本是可移动的，可以根据需要拉伸。此外，文本本身不能像文本框一样编辑。

**方法:**为了实现这一点，我们将使用一个名为 FabricJS 的 JavaScript 库。使用 CDN 导入库后，我们将在主体标签中创建一个包含文本的*画布*块。之后，我们将初始化由 FabricJS 提供的 Canvas 和 Text 的实例，并使用 **fontSize** 属性来更改字体大小，并在 Text 上渲染 Canvas，如下例所示。

**语法:**

```
 fabric.Text(text, fontSize: number); 
```

**参数:**该函数接受两个参数，如上所述，如下所述:

*   **文本:**指定要写入的文本。
*   **fontSize:** 指定字体大小。

**程序:**本示例使用 FabricJS 更改文本画布的字体大小。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <title>
        How to change the font size of
        a text canvas using Fabric.js?
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
            fontSize: 90
        });

        // Render the Textbox on Canvas
        canvas.add(text);
    </script>
</body>

</html>
```

**输出:**

![](img/ae3fd5a1cafce52c6df9185ca226fd45.png)