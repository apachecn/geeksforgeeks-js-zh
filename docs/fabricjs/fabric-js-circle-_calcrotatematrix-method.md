# fabric . js Circle _ calcrotatatrix()方法

> 原文:[https://www . geesforgeks . org/fabric-js-circle-_ calcrotatatrix-method/](https://www.geeksforgeeks.org/fabric-js-circle-_calcrotatematrix-method/)

在本文中，我们将看到如何使用 FabricJS 在画布 circle 中获取一个 Circle 对象的旋转矩阵 _ calcRotateMatrix()方法，它用于填充一个对象。画布圆意味着圆是可移动的，可以根据需要拉伸。此外，当涉及到初始笔画颜色、高度、宽度、填充颜色或笔画宽度时，可以自定义圆形。

方法用于计算圆形物体的旋转矩阵。

**方法:**首先导入 fabric.js 库。导入库后，在主体标签中创建一个包含圆形的画布块。之后，初始化 Fabric 提供的 Canvas 和 Circle 类的一个实例。JS 并使用 _ calcRotateMatrix()方法。

**语法:**

```
circle._calcRotateMatrix()
```

**参数:**该函数不取任何参数。

**返回值:**该方法返回包含对象旋转矩阵的数组。

**示例:**本示例使用 FabricJS 设置画布圆的 _ calcRotateMatrix()方法，如下例所示:

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
   <h1 style="color: green;"> 
      GeeksforGeeks 
   </h1> 

   <h3> 
      Fabric.js Circle _calcRotateMatrix() method 
   </h3> 

   <canvas id="canvas" width="600" height="300"
      style="border:1px solid #000000"> 
   </canvas> 

   <script> 

      // Initiate a Canvas instance 
      var canvas = new fabric.Canvas("canvas"); 

      // Initiate a Circle instance 
      var circle = new fabric.Circle({ 
         radius: 100, 
         fill: 'blue', 
         stroke: 'green', 
         strokeWidth: 3, 
         angle: 30 
      }); 

      // Render the circle in canvas 
      canvas.add(circle); 
      canvas.centerObject(circle); 
      console.log(circle._calcRotateMatrix())
   </script> 
</body> 

</html>
```

**输出:**

![](img/980b0c6e70b0d8f3e9de2ba74818c169.png)

**参考:**[http://fabricjs.com/docs/fabric.circle . html # _ calcrotatatrix](http://fabricjs.com/docs/fabric.Circle.html#_calcRotateMatrix)