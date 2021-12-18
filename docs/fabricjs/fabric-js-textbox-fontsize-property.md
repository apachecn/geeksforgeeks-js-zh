# Fabric.js 文本框字体大小属性

> 原文:[https://www . geesforgeks . org/fabric-js-textbox-font size-property/](https://www.geeksforgeeks.org/fabric-js-textbox-fontsize-property/)

在本文中，我们将看到如何使用 FabricJS 更改文本框画布的字体大小。文本框画布意味着所写的文本框是可移动的，可以根据需要进行拉伸。

**方法:**为了实现这一点，我们将使用一个名为 FabricJS 的 JavaScript 库。使用 CDN 导入库后，我们将在主体标签中创建一个画布块，其中将包含我们的文本框。之后，我们将初始化由 FabricJS 提供的 Canvas 和 Textbox 的实例，并使用 fontSize 属性来更改字体大小，并在 Textbox 上呈现 Canvas，如下例所示。

**语法:**

```
fabric.Textbox('text', {
    fontSize: number
});
```

**参数:**该函数接受一个参数，如上所述，如下所述:

*   **fontSize:** 指定字体大小。

**示例:**本示例使用 FabricJS 更改文本框画布的字体大小。

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
      Fabric.js | Textbox fontSize Property
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
          fontSize: 90
      });

      // Render the Textbox in canvas 
      canvas.add(text);
      canvas.centerObject(text);
  </script>
</body>

</html>
```

**输出:**

![](img/4d21743866373ec04c2cbf83ba7c63ff.png)