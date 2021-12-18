# 织物 js 路径角样式属性

> 原文:[https://www . geesforgeks . org/fabric-js-path-corner style-property/](https://www.geeksforgeeks.org/fabric-js-path-cornerstyle-property/)

在本文中，我们将看到如何使用 **Fabric.js** 设置路径画布的**角样式**。Fabric.js 中的路径是可移动的，可以根据需要进行拉伸。此外，当涉及到初始笔画颜色、高度、宽度、填充颜色或笔画宽度时，可以自定义路径。

**方法:**为了实现这一点，我们将使用一个名为 **Fabric.js** 的 JavaScript 库。导入库后，我们将在主体标签中创建一个包含路径的画布块。之后，我们将初始化 Fabric.js 提供的 Canvas 和 Path 的实例，并使用 **cornerStyle** 属性设置 canvas Path 的控制角的样式。

**语法:**

```
fabric.Path('path', {
   cornerStyle: String
});
```

**参数:**该函数接受如上所述的单个参数，如下所述:

*   **转角样式:**指定控制转角的样式。

以下示例说明了 Fabric.js **路径角样式**属性的使用:

**示例:**

## 超文本标记语言

```
<!DOCTYPE html> 
<html> 

<head>
  <!-- FabricJS CDN -->
  <script src= 
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js"> 
  </script> 
</head> 

<body> 
  <div style="text-align: center;width: 400px;"> 
    <h1 style="color: green;"> 
      GeeksforGeeks 
    </h1>
    <b> 
      Fabric.js | Path cornerStyle Property 
    </b> 
  </div> 

  <div style="text-align: center;"> 
    <canvas id="canvas" width="400" height="200"
      style="border:1px solid green;"> 
    </canvas> 
  </div> 

  <script> 
    // Initiate a Canvas instance 
    var canvas = new fabric.Canvas("canvas"); 

    var geek = new fabric.Path('M 0 0 L 100 100 L 0 100 z', {
        fill: 'green',
        cornerStyle: 'circle'
    });

    canvas.add(geek);
  </script> 
</body> 

</html>
```

**输出:**

![](img/cfbf2e50db19c48ff83af9436721db52.png)