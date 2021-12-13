# Fabric.js 线有边框属性

> 原文:[https://www . geesforgeks . org/fabric-js-line-hasborders-property/](https://www.geeksforgeeks.org/fabric-js-line-hasborders-property/)

在本文中，我们将在 **FabricJS** 中查看画布线中的边框是否可见。帆布线是指线是可移动的，可以根据需要拉伸。此外，当涉及到初始笔画颜色、高度、宽度、填充颜色或笔画宽度时，可以自定义线条。

**语法:**

```html
fabric.line({
    hasBorders: boolean
});
```

**方法:**为了实现这一点，我们将使用一个名为**的 JavaScript 库。导入库之后，我们将在主体标签中创建一个画布块，它将包含行。之后，我们将使用 **hasBorders** 属性初始化 **FabricJS** 和提供的画布和线条的实例，如果画布线条中的边框可见或不可见，则在画布上渲染线条，如下所示。**

**参数:**该函数接受如上所述的单个参数，如下所述:

*   **有边框** **:** 指定边框是否可见。它包含一个布尔值。

**例 1:**

## 超文本标记语言

```html
<!DOCTYPE html> 
<html> 

<head> 

   <script src= 
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js"> 
   </script> 
</head> 

<body> 
   <h1>fabric.js | line hasBorders  property</h1>
   <canvas id="canvas" width="600" height="200"
      style="border:1px solid #000000;"> 
   </canvas> 

   <script> 
      var canvas = new fabric.Canvas("canvas"); 

      var line = new fabric.Line([150, 10, 220, 150], { 
         stroke: 'green',
         hasBorders: true
      }); 

      canvas.add(line); 
   </script> 
</body> 

</html> 
```

**输出:**

![](img/5af50983774b8ff91a379fb0562ea9ab.png)

**例 2:**

## 超文本标记语言

```html
<!DOCTYPE html> 
<html> 

<head> 

   <script src= 
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js"> 
   </script> 
</head> 

<body> 
   <h1>fabric.js | line hasBorders  property</h1>
   <canvas id="canvas" width="600" height="200"
      style="border:1px solid #000000;"> 
   </canvas> 

   <script>
      var canvas = new fabric.Canvas("canvas"); 

      var line = new fabric.Line([150, 10, 220, 150], { 
         stroke: 'green',
         hasBorders: false
      }); 

      canvas.add(line); 
   </script> 
</body> 

</html> 
```

**输出:**

![](img/d782402dabdbaf376d58746a8e5765c3.png)