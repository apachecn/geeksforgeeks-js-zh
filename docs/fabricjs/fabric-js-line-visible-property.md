# 织物 js 线可见属性

> 原文:[https://www . geesforgeks . org/fabric-js-line-visible-property/](https://www.geeksforgeeks.org/fabric-js-line-visible-property/)

在本文中，我们将使用*可见* 属性来设置画布线条在 **FabricJS** 中的可见性。帆布线是可移动的，可以根据需要拉伸。此外，对于初始笔画*颜色、高度、宽度、填充颜色、*或*笔画宽度，可以自定义线条。*

**语法:**

```html
fabric.line({
    visible: boolean
});
```

**方法:**为了实现这一点，我们将使用一个名为**的 JavaScript 库。导入库之后，我们将在主体标签中创建一个画布块，它将包含行。之后，我们将初始化 **FabricJS** 和提供的画布和线条实例，使用*可见*属性设置画布线条的可见性，并在画布上渲染线条，如下所示。**

**参数:**该函数接受一个参数，如上所述，如下所述。

*   **可见:**指定画布线的可见性。包含布尔值。

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
   <h1>fabric.js | line visible property</h1>

   <canvas id="canvas" width="600" height="200"
      style="border:1px solid #000000;"> 
   </canvas> 

   <script> 
      var canvas = new fabric.Canvas("canvas"); 

      var line = new fabric.Line([150, 10, 220, 150], { 
         stroke: 'green',
         visible : false
      }); 
      canvas.add(line); 
   </script> 
</body> 

</html> 
```

**输出:**

![](img/75e16a8758c9b95e8397f0ae0d27679e.png)

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
   <h1>fabric.js | line visible property</h1>

   <canvas id="canvas" width="600" height="200"
      style="border:1px solid #000000;"> 
   </canvas> 

   <script> 
      var canvas = new fabric.Canvas("canvas"); 

      var line = new fabric.Line([150, 10, 220, 150], { 
         stroke: 'green',
         visible : true
      }); 

      canvas.add(line); 
   </script> 
</body> 

</html> 
```

**输出:**

![](img/e33704f044c80db87ecfd07087a2d140.png)