# Fabric.js 文本框包含错误值属性

> 原文:[https://www . geesforgeks . org/fabric-js-textbox-includefaultvalues-property/](https://www.geeksforgeeks.org/fabric-js-textbox-includedefaultvalues-property/)

在本文中，我们将看到如何使用 FabricJS 设置 Textbox 画布的 includeDefaultValues 属性。画布文本框意味着文本框是可移动的，可以根据需要进行拉伸。此外，当涉及到初始笔画颜色、高度、宽度、填充颜色或笔画宽度时，可以自定义文本框。

为了实现这一点，我们将使用一个名为 FabricJS 的 JavaScript 库。导入库后，我们将在主体标签中创建一个包含文本框的画布块。之后，我们将初始化由 FabricJS 提供的 canvas 和 Textbox 的实例，并使用 includeDefaultValues 属性设置 canvas textbox 的 includeDefaultValues，并在 Canvas 上呈现文本框，如下例所示。

**语法:**

```
fabric.Textbox('text', {
    includeDefaultValues: boolean
});
```

**参数:**该函数接受一个参数，如上所述，如下所述:

*   **包含默认值:**指定包含在文本框中的默认值。

**注意:**如果 includeDefaultValues 属性设置为 **false，**默认对象的值不包含在其序列化中。

**示例:**本示例使用 FabricJS 设置画布文本框的 includeDefaultValues 属性。

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
      Fabric.js | Textbox includeDefaultValues Property
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
          includeDefaultValues: true
      });

      // Render the Textbox in canvas 
      canvas.add(text);
      canvas.centerObject(text);
  </script>
</body>

</html>
```

**输出:**

![](img/aa99a22856e891a6bc81e8816ee9ad30.png)