# Fabric.js matrixToSVG()方法

> 原文:[https://www.geeksforgeeks.org/fabric-js-matrixtosvg-method/](https://www.geeksforgeeks.org/fabric-js-matrixtosvg-method/)

**matrixToSVG()方法**用于为某些数字的指定数组返回类似**“矩阵(…数字)”**的内容。

**语法:**

```
matrixToSVG(transform)
```

**参数:**该方法接受如上所述的参数，如下所述:

*   **变换:**此参数保存包含一些数字的指定数组。

**返回值:**该方法返回 SVG 的变换矩阵，类似于**“矩阵(…数字)”**。

**例 1:**

## java 描述语言

```
<!DOCTYPE html>
<html>

<head>
    <script src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js">
    </script>

    <script type="text/javascript" src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.js">
    </script>
</head>

<body>
    <script type="text/javascript">

        // Calling matrixToSVG() function over
        // the specified arrays
        console.log(fabric.util.matrixToSVG(
                [1, 2, 3, 4, 5, 6]));
        console.log(fabric.util.matrixToSVG([0]));
        console.log(fabric.util.matrixToSVG([2, 4, 6]));
    </script>
</body>

</html>
```

**输出:**

```
matrix(1 2 3 4 5 6)
matrix(0)
matrix(2 4 6)
```

**例 2:**

## java 描述语言

```
<!DOCTYPE html>
<html>

<head>
    <script src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js">
    </script>

    <script type="text/javascript" src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.js">
    </script>
</head>

<body>
    <script type="text/javascript">

        // Specifying some arrays
        var a = [2, 4];
        var b = [0.1, 2.4];
        var c = [1, 3, 5, 7];

        // Calling matrixToSVG() function over
        // the above specified arrays
        console.log(fabric.util.matrixToSVG(a));
        console.log(fabric.util.matrixToSVG(b));
        console.log(fabric.util.matrixToSVG(c));
    </script>
</body>

</html>
```

**输出:**

```
matrix(2 4)
matrix(0.1 2.4)
matrix(1 3 5 7)
```