# Fabric.js 文本框可选属性

> 原文:[https://www . geesforgeks . org/fabric-js-textbox-selected-property/](https://www.geeksforgeeks.org/fabric-js-textbox-selectable-property/)

在本文中，我们将看到如何设置可选属性，该属性用于选择使用 FabricJS 编辑文本框画布的对象。画布文本框意味着文本框是可移动的，可以根据需要进行拉伸。此外，当涉及到初始笔画颜色、高度、宽度、填充颜色或笔画宽度时，可以自定义文本框。

为了实现这一点，我们将使用一个名为 FabricJS 的 JavaScript 库。导入库后，我们将在主体标签中创建一个包含文本框的画布块。之后，我们将初始化由 FabricJS 提供的 canvas 和 Textbox 的实例，并设置 canvas Textbox 的可选属性，以使用可选属性选择 canvas 对象，并在 Canvas 上呈现 Textbox，如下例所示。

**语法:**

```
fabric.Textbox('text', {
   selectable: Boolean
});
```

**参数:**该函数接受一个参数，如上所述，如下所述:

*   **可选:**指定对象是否可选。

**示例:**本示例使用 FabricJS 可选属性创建不可选择的对象画布文本框。

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
      Fabric.js | Textbox selectable Property
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
          selectable: false
      });

      // Render the Textbox in canvas 
      canvas.add(text);
      canvas.centerObject(text);
  </script>
</body>

</html>
```

**输出:**

![](img/7c78c1b59f0e9b2c3522ee0df871efc1.png)