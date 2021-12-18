# fabric . js Itext touchCornerSize 属性

> 原文:[https://www . geesforgeks . org/fabric-js-itext-touchcornersize-property/](https://www.geeksforgeeks.org/fabric-js-itext-touchcornersize-property/)

**Fabric.js** 是一个用来处理画布的 JavaScript 库。画布 *Itext* 是 **fabric.js** 的一个类，用于创建 *Itext* 实例。画布 *Itext* 表示 *Itext* 可移动，可根据需要拉伸。在本文中，我们将使用 *touchCornerSize* 属性在画布 *Itext* 中设置角大小。

首先导入 **fabric.js** 库。导入库后，在主体标签中创建一个包含 *Itext* 的画布块。之后，初始化画布实例和**织物提供的 *Itext* 类。JS** 并使用 *touchCornerSize* 属性设置拐角尺寸。

**语法**:

```
fabric.Itext (Itext , {
touchCornerSize : number
});
```

**参数**:该功能取一个参数，如上所述，如下所述。

*   **touchCornerSize** :该参数取数值。检测到触摸交互时对象控制角的大小。

**示例**:本示例使用 **FabricJS** 设置画布 *Itext* 的 *touchCornerSize* 属性，如下例所示。

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
      Fabric.js | Itext touchCornerSize Property 
    </b> 
  </div> 

  <div style="text-align:center;"> 
    <canvas id="canvas" width="400" height="200"
      style="border:1px solid green;"> 
    </canvas> 
  </div> 

  <script> 
    var canvas = new fabric.Canvas("canvas"); 
    var itext = new fabric.IText('GeeksforGeeks', {
            touchCornerSize : 10
    });
    canvas.add(itext);
    canvas.centerObject(itext); 
  </script> 
</body> 

</html>
```

**输出:**

![](img/ee7ee28e2f0270d60b2394d84218799c.png)