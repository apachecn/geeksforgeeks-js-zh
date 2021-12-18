# 织物 js 组锁定旋转属性

> 原文:[https://www . geesforgeks . org/fabric-js-group-lock rotation-property/](https://www.geeksforgeeks.org/fabric-js-group-lockrotation-property/)

在本文中，我们将看到如何使用 **Fabric.js** 设置画布的**组**的*锁定旋转*。**织物 js** 中的组是可移动的，可以根据需要拉伸。此外，当涉及到初始笔划*颜色、高度、宽度、填充颜色、*或*笔划宽度时，可以自定义该组。*

为了实现这一点，我们将使用一个名为 **Fabric.js** 的 JavaScript 库。导入库后，我们将在包含组的主体标签中创建画布块。之后，我们将初始化由 **Fabric.js** 提供的画布和组的实例，并使用*锁定旋转*属性锁定画布组的旋转。

**语法:**

```
fabric.Group([canvas1, canvas2], {
   lockRotation: Boolean
});
```

**参数:**该属性接受一个参数，如上所述，如下所述。

*   **锁定旋转:**指定是否锁定画布的旋转。

以下示例说明了在 JavaScript 中使用**fabric . js**Group*lock rotation*属性。

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
          Fabric.js | Group lockRotation Property
      </b>
    </div>

    <div style="text-align: center;">
      <canvas id="canvas" width="500" height="300"
      style="border:1px solid green;">
      </canvas>
    </div>

    <script>
      // Initiate a Canvas instance
      var canvas = new fabric.Canvas("canvas");

      // Initiate a circle instance
      var circle = new fabric.Circle({
        radius: 100,
        fill: 'lightgreen',
        scaleY: 0.6,
        originX: 'center',
        originY: 'center'
      });

      // Initiate a text instance
      var text = new fabric.Text('GeeksforGeeks', {
        fontSize: 25,
        originX: 'center',
        originY: 'center'
      });

      // Initiate a Group instance
      var group = new fabric.Group([ circle, text ], {  
        lockRotation : true 
      });

      // Render the Group in canvas
      canvas.add(group);

      canvas.centerObject(group);
  </script>
</body>

</html>
```

**输出:**

![](img/480a77a4708e0afeab9c937dd579026a.png)