# 织物. js 图像背景颜色属性

> 原文:[https://www . geesforgeks . org/fabric-js-image-background color-property/](https://www.geeksforgeeks.org/fabric-js-image-backgroundcolor-property/)

**Fabric.js 是**一个用来处理画布的 javascript 库。Image 是 fabric.js 的一个类，用于创建图像实例。图像的 backgroundColor 属性用于设置图像的背景颜色。

**方法:**首先导入 fabric.js 库。导入库后，在主体标签中创建一个包含图像的画布块。之后，初始化一个由 Fabric 提供的 Canvas 和 image 类的实例。JS 并使用图像对象的 background color 属性设置图像的背景颜色。

**语法:**

```
fabric.Image(image, {
   backgroundColor:"string"
});

```

**参数:**上述函数取两个参数，如上所述，描述如下:

*   **图像:**该参数保持图像。
*   **backgroundColor:** 设置图像的背景颜色。

**示例 1:** 本示例使用 FabricJS 设置画布图像的背景颜色，如下例所示。

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
    <b>Fabric.js | Image backgroundColor Property </b> 

    <canvas id="canvas" width="400" height="300"
        style="border:2px solid #000000"> 
    </canvas> 

    <img src =
 "https://media.geeksforgeeks.org/wp-content/uploads/20200327230544/g4gicon.png" 
    width="100" 
    height="100"
    id="my-image">

    <script> 

        // Create the instance of canvas object
        var canvas = new fabric.Canvas("canvas"); 
        var img= document.getElementById('my-image');
        var imgInstance = new fabric.Image(img, {
            opacity:0.8,
            backgroundColor:"yellow"
        });
        canvas.add(imgInstance);
    </script> 
</body> 

</html>
```

**输出:**

![](img/f4d0c3f6b015b2ded610b54717bb7789.png)

**例 2:**

## 超文本标记语言

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
    <b>Fabric.js | Image backgroundColor Property </b> 

    <canvas id="canvas" width="300" height="200"
        style="border:2px solid #000000"> 
    </canvas> 

    <img src =
"https://www.geeksforgeeks.org/wp-content/uploads/gfg_200X200-1.png" 
    width="100" 
    height="100"
    id="my-image"
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
            // Create the instance of canvas object
            var canvas = new fabric.Canvas("canvas"); 
            var img= document.getElementById('my-image');
            var imgInstance = new fabric.Image(img, {
                opacity:0.4,
                backgroundColor:"green"
            });
            canvas.clear();
            canvas.add(imgInstance);
        }
    </script> 
</body> 

</html>
```

**输出:**

*   **点击点击我按钮前:**

![](img/7d8ba36825b993826dfc4f955e3b335b.png)

*   **点击点击我按钮后:**

![](img/cd5e72537d4586f77c41c319543df699.png)