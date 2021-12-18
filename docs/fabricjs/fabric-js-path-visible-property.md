# 织物. js 路径可见属性

> 原文:[https://www . geesforgeks . org/fabric-js-path-visible-property/](https://www.geeksforgeeks.org/fabric-js-path-visible-property/)

在本文中，我们将看到如何使用 **Fabric.js** 设置路径的*可见*属性。**布艺. js** 中的路径是可移动的，可以根据需要拉伸。此外，在初始*笔画颜色、高度、宽度、填充颜色、*或*笔画宽度*时，可以自定义路径。

为了实现这一点，我们将使用一个名为 **Fabric.js** 的 JavaScript 库。导入库后，我们将在主体标签中创建一个包含路径的画布块。之后，我们将初始化由 **Fabric.js** 提供的画布和路径的实例，并使用 **visible** 属性来切换可见性和渲染画布路径。

**语法:**

```
fabric.Path('path', {
   visible: Boolean
});
```

**参数:**该函数接受一个参数，如上所述，如下所述。

*   **可见:**指定对象的可见性。它包含一个布尔值。如果设置为“假”，则不呈现对象。

下面的例子说明了在 JavaScript 中使用 Fabric.js **路径** *可见*属性。

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
      Fabric.js | Path visible Property 
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
      visible: false
    });

    canvas.add(geek);
  </script> 
</body> 

</html>
```

**输出:**

![](img/7ba728f3d3f27cf8a46297ca8d6447fb.png)

在上面的代码中，当 Fabric.js **路径** *可见*属性设置为*真*时，将显示以下输出。

![](img/107a294993ae867f3aae4120370b2454.png)