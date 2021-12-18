# Fabric.js invertTransform()方法

> 原文:[https://www . geesforgeks . org/fabric-js-invert transform-method/](https://www.geeksforgeeks.org/fabric-js-inverttransform-method/)

**反变换()方法**用于返回指定数组变换的反形式。该函数计算数组元素的逐位反转。

**语法:**

```
invertTransform(t)
```

**参数:**该方法接受如上所述的参数，如下所述:

*   **t:** 此参数保存指定的数组变换。

**返回值:**此方法返回指定数组变换的反转形式。

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

        // Calling invertTransform() function over
        // some array transform
        console.log(fabric.util
            .invertTransform([1, 2, 3]));

        console.log(fabric.util
            .invertTransform([1, 2, 3, 4]));

        console.log(fabric.util
            .invertTransform([1, 2, 3, 4, 5]));

        console.log(fabric.util
            .invertTransform([1, 2, 3, 4, 5, 6]));
    </script>
</body>

</html>
```

**输出:**

```
[null,null,null,null,null,null]
[-2,1,1.5,-0.5,null,null]
[-2,1,1.5,-0.5,null,null]
[-2,1,1.5,-0.5,1,-2]
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

        // Specifying some arrays
        var array1 = [5, 10, 15, 20];
        var array2 = [1, 3, 5, 7, 9, 11];

        // Calling invertTransform() function
        // over the above array transform
        console.log(fabric.util.invertTransform(array1));
        console.log(fabric.util.invertTransform(array2));
    </script>
</body>

</html>
```

**输出:**

```
[-0.4,0.2,0.3,-0.1,null,null]
[-0.875,0.375,0.625,-0.125,1,-2]
```