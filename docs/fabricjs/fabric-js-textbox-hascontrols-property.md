# 织物. js 文本框具有控件属性

> 原文:[https://www . geesforgeks . org/fabric-js-textbox-has controls-property/](https://www.geeksforgeeks.org/fabric-js-textbox-hascontrols-property/)

在本文中，我们将看到如何使用 FabricJS 禁用画布文本框的操作。画布意味着文本框是可移动的，可以根据需要拉伸。此外，文本框可以自定义初始笔画颜色、填充颜色、笔画宽度或半径。

**方法:**为了使其成为可能，我们将使用一个名为 FabricJS 的 JavaScript 库。使用 CDN 导入库后，我们将在主体标签中创建一个画布块，其中将包含我们的文本框。之后，我们将初始化由 FabricJS 提供的 Canvas 和 Textbox 的实例，并使用 hasControls 属性禁用对 Textbox 的操作，并在 Canvas 上呈现 Textbox，如下例所示。

**语法:**

```
fabric.Textbox('text', {
    hasControls: boolean
});
```

**参数:**该函数接受一个参数，如上所述，如下所述:

*   **有控制:**指定是否禁用控制。

**示例:**本示例使用 **FabricJS** 禁用画布文本框的操作。注意你必须点击物体才能看到角落。

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
      Fabric.js | Textbox hasControls Property
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
          hasControls: false
      });

      // Render the Textbox in canvas 
      canvas.add(text);
      canvas.centerObject(text);
  </script>
</body>

</html>
```

**输出:**

![](img/3611b465bbaae74b04032888b011f5c4.png)