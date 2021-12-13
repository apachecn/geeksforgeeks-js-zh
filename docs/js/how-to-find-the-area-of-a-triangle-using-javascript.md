# 如何用 JavaScript 找到三角形的面积？

> 原文:[https://www . geesforgeks . org/如何使用 javascript 找到三角形区域/](https://www.geeksforgeeks.org/how-to-find-the-area-of-a-triangle-using-javascript/)

给定一个包含输入字段的 HTML 文档，输入字段包含三角形的边，即边 1、边 2 和边 3。任务是用 JavaScript 找到三角形的面积。

**方法:**首先我们将使用<输入类型=“数字”>标签创建三个输入字段来保存数字输入。填写完输入值后，当用户点击按钮时，就会调用 JavaScript 函数 Area()。

在 JavaScript 函数中，我们使用**document . getelementbyid(“side 1”)。值**获取输入值，然后对其应用**parsent()**方法获取数字形式的输入值。然后用简单的数学公式求出三角形的面积，用 **document.getElementById(“显示”)。innerHTML** 在屏幕上显示输出。

**求三角形面积的公式:**

```html
var s = (side1 + side2 + side3) / 2;

var area = Math.sqrt(s * ((s - side1) * (s - side2) * (s - side3)));
```

**示例:**

## 超文本标记语言

```html
<!DOCTYPE HTML>
<html>

<head>
    <meta http-equiv="Content-Type" 
        content="text/html; charset=utf-8">

    <title>
        JavaScript function to find 
        the area of a triangle
    </title>
</head>

<body style="text-align: center;">
    <h1 style="color: green;">
        GeeksforGeeks
    </h1>

    <h4>
        JavaScript function to find 
        the area of a triangle
    </h4>

    <label for="side1">
        Enter the value of side 1: 
    </label>

    <input type="number" id="side1" 
        placeholder="Enter value of side 1">
    <br><br>

    <label for="side2">
        Enter the value of side 2: 
    </label>

    <input type="number" id="side2" 
        placeholder="Enter value of side 2">
    <br><br>

    <label for="side3">
        Enter the value of side 3: 
    </label>

    <input type="number" id="side3" 
        placeholder="Enter value of side 2">
    <br><br>

    <button onclick="Area()">Click Here!</button>

    <p>
        Area of Triangle: <span id="display"></span>
    </p>

    <script type="text/javascript">
        function Area() {
            var side1 = parseInt(document
                .getElementById("side1").value);

            var side2 = parseInt(document
                .getElementById("side2").value);

            var side3 = parseInt(document
                .getElementById("side3").value);

            console.log(typeof(side1));
            var s = (side1 + side2 + side3) / 2;

            var area = Math.sqrt(s * ((s - side1) 
                    * (s - side2) * (s - side3)));

            document.getElementById(
                "display").innerHTML = area;
        }
    </script>
</body>

</html>
```

**输出:**

![](img/4e55041b541e7161cb7f22c8fce179b0.png)