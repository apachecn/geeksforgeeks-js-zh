# fabric . js qrDefault()方法

> 原文:[https://www.geeksforgeeks.org/fabric-js-qrdecompose-method/](https://www.geeksforgeeks.org/fabric-js-qrdecompose-method/)

**qrdinate()方法**用于将指定的标准 2×3 矩阵分解成变换分量

**语法:**

```
qrDecompose( mat )
```

**参数:**该方法接受如上所述的参数，如下所述:

*   **mat:** 此参数保存指定的变换矩阵数组。

**返回值:**该方法返回变换的分量。

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

        // Calling qrDecompose() function over
        // the specified array of transform matrix
        console.log(fabric.util
            .qrDecompose([1, 2, 3, 4, 5, 6]));
    </script>
</body>

</html>
```

**输出:**

```
{"angle":63.434948822922,"scaleX":2.23606797749979,"scaleY":-0.8944271909999159,
"skewX":65.55604521958347,"skewY":0,"translateX":5,"translateY":6}
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

        // Specifying some array of transform matrix
        var a1 = [1, 2, 3];
        var a2 = [0, 6, 7, 8, 0, 0];

        // Calling qrDecompose() function over the
        // above specified array of transform matrix
        console.log(fabric.util.qrDecompose(a1));
        console.log(fabric.util.qrDecompose(a2));
    </script>

</body>

</html>
```

**输出:**

```
{"angle":63.434948822922,"scaleX":2.23606797749979,"scaleY":null,"skewX":null,"skewY":0}
{"angle":90,"scaleX":6,"scaleY":-7,"skewX":53.13010235415598,"skewY":0,
"translateX":0,"translateY":0}
```