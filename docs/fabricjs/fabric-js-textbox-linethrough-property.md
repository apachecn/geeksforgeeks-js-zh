# Fabric.js Textbox linethrough 属性

> 原文:[https://www . geesforgeks . org/fabric-js-textbox-line through-property/](https://www.geeksforgeeks.org/fabric-js-textbox-linethrough-property/)

在本文中，我们将看到如何使用 FabricJS 中的 **linethrough** 属性在画布 Textbox 中添加一行。画布意味着所写的文本框是可移动的，可以根据需要进行拉伸、调整大小和旋转。此外，文本本身不能像文本框一样编辑。

**进场:**

*   为了实现这一点，我们将使用一个名为 FabricJS 的 JavaScript 库。
*   使用 CDN 导入库后，我们将在主体标签中创建一个画布块，其中将包含我们的文本框。
*   之后，我们将初始化由 FabricJS 提供的 Canvas 和 Textbox 的实例，并使用 linethrough 属性添加一个 linethrough，并在 Textbox 上呈现 Canvas，如下例所示。

**语法:**

```
fabric.Textbox('text', {
    linethrough: boolean
});
```

**参数:**该函数接受一个参数，如上所述，如下所述:

*   **linethrough:** 是一个布尔值，指定是启用还是禁用 linethrough 文本修饰，默认情况下禁用。

**示例:**我们将使用 FabricJS 向文本框画布中的文本添加 linethrough，如下所示

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
      Fabric.js | Textbox linethrough Property
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
         linethrough: true
      });

      // Render the Textbox in canvas 
      canvas.add(text);
      canvas.centerObject(text);
   </script>
</body>

</html>
```

**输出:**

![](img/19c62849b6674779f0ca3f1df17228a5.png)