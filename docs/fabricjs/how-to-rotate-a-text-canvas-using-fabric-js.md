# 如何使用 Fabric.js 旋转文本画布？

> 原文:[https://www . geeksforgeeks . org/如何旋转文本-画布-使用织物-js/](https://www.geeksforgeeks.org/how-to-rotate-a-text-canvas-using-fabric-js/)

在本文中，我们将看到如何使用 FabricJS 旋转文本画布。画布意味着书写的文本是可移动的，可以根据需要拉伸。此外，文本本身不能像文本框一样编辑。
**方法:**为了实现这一点，我们将使用一个名为 FabricJS 的 JavaScript 库。使用 CDN 导入库后，我们将在主体标签中创建一个包含文本的*画布*块。之后，我们将初始化 FabricJS 提供的 Canvas 和 text 的实例，并使用 **angle** 属性将文本旋转到所需的角度，并在 Text 上渲染 Canvas，如下例所示。

**语法:**

```
fabric.Text(text, angle: Number); 
```

**参数:**该函数接受两个参数，如上所述，如下所述:

*   **文本:**指定要写入的文本。
*   **选项:**它指定了要应用的附加选项，我们在这个例子中使用了角度选项。

**程序:**本示例使用 FabricJS 创建简单的可编辑文本画布。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <title>
        How to rotate a text canvas using Fabric.js?
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
            angle: 10
        });

        // Render the Textbox on Canvas
        canvas.add(text);
    </script>
</body>

</html>
```

**输出:**

![](img/1cb7b657759a2a56d2657cc68b58c6db.png)