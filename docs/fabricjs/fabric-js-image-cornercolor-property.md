# 织物. js 图像角色属性

> 原文:[https://www . geesforgeks . org/fabric-js-image-corner color-property/](https://www.geeksforgeeks.org/fabric-js-image-cornercolor-property/)

**Fabric.js** 是一个用来处理画布的 javascript 库。Image 是 fabric.js 的一个类，用于创建图像实例。图像的 cornerColor 属性用于更改图像的控制角的颜色。

**方法:**首先导入 fabric.js 库。导入库后，在主体标签中创建一个包含图像的画布块。之后，初始化一个由 Fabric 提供的 Canvas 和 image 类的实例。JS 并使用图像对象的 cornerColor 属性设置图像控制器的 cornerColor。

**语法:**

```
fabric.Image(image, {
    cornerColor:string
});

```

**参数:**上述函数取两个参数，如上所述，描述如下:

*   **图像:**该参数取图像。
*   **角颜色:**设置图像的控制角颜色。

**示例 1:** 本示例使用 FabricJS 设置画布图像的控制角颜色，如下例所示。

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
    <h1 style="color: green;">GeeksforGeeks</h1> 
    <b>Fabric.js | Image cornerColor Property </b> 

    <canvas id="canvas" width="400" height="300"
        style="border:2px solid #000000"> 
    </canvas> 

    <img src =
"https://media.geeksforgeeks.org/wp-content/uploads/20200327230544/g4gicon.png" 
        width="100" height="100" id="my-image"
        style="display: none;">

    <script> 

        // Create the instance of canvas object
        var canvas = new fabric.Canvas("canvas"); 
        var img= document.getElementById('my-image');
        var imgInstance = new fabric.Image(img, {
            cornerColor:"red"
        });
        canvas.add(imgInstance);
    </script> 
</body> 

</html>
```

**输出:**

![](img/ba75047877420378ca15800e53733b3b.png)

**例 2:**

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
    <h1 style="color: green;">GeeksforGeeks</h1> 
    <b>Fabric.js | Image cornerColor Property </b> 

    <canvas id="canvas" width="300" height="250"
        style="border:2px solid #000000"> 
    </canvas> 

    <img src =
"https://www.geeksforgeeks.org/wp-content/uploads/gfg_200X200-1.png" 
        width="100" height="100" id="my-image"
        style="display:none">
    <br>

    <button onclick="func()">Clickme</button>

    <script> 

        // Create the instance of canvas object
        var canvas = new fabric.Canvas("canvas"); 
        var img= document.getElementById('my-image');
        var imgInstance = new fabric.Image(img, {
        });
        canvas.add(imgInstance);
        func=()=>{
            var imgInstance = new fabric.Image(img, {
                cornerColor:"green"
            });
            canvas.clear();
            canvas.add(imgInstance);
        }
    </script> 
</body> 

</html>
```

**输出:**

![](img/c8f636f1355fb5ada45e4d8efc47b998.png)