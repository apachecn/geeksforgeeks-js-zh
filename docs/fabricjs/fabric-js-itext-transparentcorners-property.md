# Fabric.js Itext 透明角落属性

> 原文:[https://www . geesforgeks . org/fabric-js-itext-transparentcorners-property/](https://www.geeksforgeeks.org/fabric-js-itext-transparentcorners-property/)

**Fabric.js** 是一个用来处理画布的 JavaScript 库。画布 *Itext* 是用于创建 *Itext* 实例的 **fabric.js** 类之一。画布 *Itext* 表示 Itext 是可移动的，可以根据需要拉伸。

在本文中，我们将使用*透明角*属性来设置角在画布 Itext 中是否透明。

首先导入 **fabric.js** 库。导入库后，在主体标签中创建一个包含 Itext 的画布块。之后，初始化画布的一个实例和由 **Fabric.js** 提供的 *Itext* 类，并使用 *transparentCorners* 属性设置角是否透明。

**语法**:

```html
fabric.Itext (Itext , {
    transparentCorners : boolean
});
```

**参数**:该功能取一个参数，如上所述，如下所述。

*   **透明角落**:该参数取布尔值。

**例**:本例使用**面料。JS** 设置画布 Itext 的*透明角落*属性，如下例所示。

## 超文本标记语言

```html
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
      Fabric.js | Itext transparentCorners Property 
    </b> 
  </div> 

  <div style="text-align: center;"> 
    <canvas id="canvas" width="400" height="200"
      style="border:1px solid green;"> 
    </canvas> 
  </div> 

  <script> 
    var canvas = new fabric.Canvas("canvas"); 

    var geek = new fabric.IText('GeeksforGeeks', {
            transparentCorners : false
    });
    canvas.add(geek);
    canvas.centerObject(geek); 
  </script> 
</body> 

</html>
```

**输出:**

![](img/0c2d96932defcbd5d7651274bc96b3b3.png)

如果在上面的代码中*透明角落*属性被设置为*真*，输出如下。

![](img/cfc0656ddaff3ce3e6d1234e9513946f.png)