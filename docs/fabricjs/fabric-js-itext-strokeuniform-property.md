# 织物硬度均匀性

> 原文:[https://www . geesforgeks . org/fabric-js-itext-stroke uniform-property/](https://www.geeksforgeeks.org/fabric-js-itext-strokeuniform-property/)

Fabric.js 是一个用于处理画布的 JavaScript 库。画布 Itext 是用于创建 Itext 实例的 Fabric.js 类之一。画布 Itext 是指 Itext 是可移动的，可以根据需要拉伸。在本文中，我们将使用 **strokeUniform** 属性，这样即使我们将对象缩放到更大的尺寸，笔画的宽度也保持不变。

首先导入 Fabric.js 库。导入库后，在主体标签中创建一个包含 Itext 的画布块。之后，初始化一个由 Fabric.js 提供的 Canvas 和 Itext 类的实例，并使用 **strokeUniform** 属性。

**语法:**

```
fabric.Itext(Itext, {
  strokeUniform: boolean
});
```

**参数:**该函数采用如上所述的单个参数，描述如下:

*   **笔画均匀:**该参数取一个布尔值，决定笔画的宽度是否均匀。

**示例:**本示例使用 Fabric.js 设置画布 Itext 的 strokeUniform 属性。

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
  <div style="text-align: center;
              width: 400px;"> 
    <h1 style="color: green;"> 
      GeeksforGeeks 
    </h1>
    <b> 
      Fabric.js | Itext strokeUniform Property 
    </b> 
  </div> 
  <div style="text-align: center;"> 
    <canvas id="canvas" 
            width="400" height="200"
      style="border:1px solid green;"> 
    </canvas> 
  </div> 
  <script> 
    var canvas = new fabric.Canvas("canvas"); 

    var geek = new fabric.IText('GeeksforGeeks', {
        strokeUniform : true
    });

    console.log(geek.strokeUniform)
    canvas.add(geek);
    canvas.centerObject(geek); 
  </script> 
</body> 
</html>
```

**输出:**

![](img/5591a183ddacc55ec21644f313c49eb4.png)