# Fabric.js limitDimsByArea()方法

> 原文:[https://www . geesforgeks . org/fabric-js-limitdimsbyarea-method/](https://www.geeksforgeeks.org/fabric-js-limitdimsbyarea-method/)

**limitDimsByArea()方法**用于返回最大宽度和高度，该最大宽度和高度可以考虑指定纵横比的总允许面积。纵横比描述图像、屏幕或区域的宽度和高度之间的比率。例如，1:1 的长宽比，就是一个正方形。第一个数字总是指宽度，第二个数字指高度。在这个函数中，长宽比被描述为一个数字——在这个例子中，数字是指宽度，而高度是 1。

**语法:**

```
limitDimsByArea(ar, maximumArea)
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **ar:** 此参数保持指定的纵横比。
*   **最大值:**此参数保存允许的面积。

**返回值:**该方法按宽度(x)和高度(y)返回限定尺寸。

**例 1:**

## java 描述语言

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
    <script type="text/javascript">

        // Calling limitDimsByArea() function over
        // the specified aspect ratios and areas
        console.log(fabric.util.limitDimsByArea(1, 5));
        console.log(fabric.util.limitDimsByArea(2, 20));
        console.log(fabric.util.limitDimsByArea(5, 45));
        console.log(fabric.util.limitDimsByArea(10, 500));
    </script>
</body>

</html>
```

**输出:**

```
{"x":2,"y":2}
{"x":6,"y":3}
{"x":15,"y":3}
{"x":70,"y":7}
```

**例 2:**

## java 描述语言

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
    <script type="text/javascript">

        // Specifying some aspect ratios and areas
        var ar1 = 4;
        var ar2 = 6;
        var area1 = 50;
        var area2 = 100;

        // Calling limitDimsByArea() function over
        // the above specified aspect ratios and areas
        console.log(fabric.util.limitDimsByArea(ar1, area1));
        console.log(fabric.util.limitDimsByArea(ar2, area2));
    </script>
</body>

</html>
```

**输出:**

```
{"x":14,"y":3}
{"x":24,"y":4}
```