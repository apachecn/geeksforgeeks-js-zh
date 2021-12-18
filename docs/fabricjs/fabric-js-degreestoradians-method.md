# 面料. js 度数弧度()方法

> 原文:[https://www . geesforgeks . org/fabric-js-degreestorands-method/](https://www.geeksforgeeks.org/fabric-js-degreestoradians-method/)

**degreestorands()方法**用于将指定度数的值转换为其对应的弧度值。

**语法:**

```
degreesToRadians( degrees )
```

**参数:**该方法接受如上所述的参数，如下所述:

*   **度:**此参数保存指定的度值。

**返回值:**此方法返回转换后的弧度值。

**例 1:**

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
    <script type="text/javascript">

        // Calling degreesToRadians() function over
        // some specified degree values
        console.log(fabric.util.degreesToRadians(30));
        console.log(fabric.util.degreesToRadians(45));
        console.log(fabric.util.degreesToRadians(90));
    </script>
</body>

</html>
```

**输出:**

```
0.5235987755982988
0.7853981633974483
1.5707963267948966
```

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
    <script type="text/javascript">

        // Specifying some degree values
        var a = 0;
        var b = 10;

        // Calling degreesToRadians() function over
        // above specified degree vlaue
        console.log(fabric.util.degreesToRadians(a));
        console.log(fabric.util.degreesToRadians(b));
    </script>
</body>

</html>
```

**输出:**

```
0
0.17453292519943295
```