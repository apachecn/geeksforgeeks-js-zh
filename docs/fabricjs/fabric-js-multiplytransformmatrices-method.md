# fabric . js multiplytransformmatrix()方法

> 原文:[https://www . geesforgeks . org/fabric-js-multiplytransformmatrix-method/](https://www.geeksforgeeks.org/fabric-js-multiplytransformmatrices-method/)

**multiplytransformmatrix()方法**用于将两个指定的矩阵相乘以嵌套变换。例如，如果函数为 multiplyTransformMatrices，b)，则表示矩阵 **a** 将乘以矩阵 **b** 。

**语法:**

```
multiplyTransformMatrices(a, b, is2x2)
```

**参数:**该方法接受如上所述的参数，如下所述:

*   **a:** 该参数保存第一个指定的变换矩阵。
*   **b:** 此参数保存第二个指定的变换矩阵。
*   **为 2x2:** 该参数为布尔值，保存将矩阵相乘为 2×2 矩阵的标志。

**返回值:**该方法返回两个指定变换矩阵的乘积。

**例 1:**

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
  <script src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js" >
  </script>

  <script type="text/javascript" src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js.map">
  </script>

  <script type="text/javascript" src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.js">
  </script>
</head>

<body>
  <script type="text/javascript">
    // Calling multiplyTransformMatrices() function over
    // some specified arrays
    console.log(fabric.util.multiplyTransformMatrices([1, 2], [3, 4]));
    console.log(fabric.util.multiplyTransformMatrices([1, 2], [3, 4], true));
    console.log(fabric.util.multiplyTransformMatrices([1, 2], [3, 4], false));
    console.log(fabric.util.multiplyTransformMatrices([1, 2, 3, 4],
                                                      [5, 6, 7, 8]));
    console.log(fabric.util.multiplyTransformMatrices([1, 2, 3, 4],
                                                      [5, 6, 7, 8], true));
    console.log(fabric.util.multiplyTransformMatrices([1, 2, 3, 4],
                                                      [5, 6, 7, 8], false));
  </script>
</body>

</html>
```

**输出:**

```
[null,null,null,null,null,null]
[null,null,null,null,0,0]
[null,null,null,null,null,null]
[23,34,31,46,null,null]
[23,34,31,46,0,0]
[23,34,31,46,null,null]
```

**例 2:**

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
  <script src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js" >
  </script>

  <script type="text/javascript" src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js.map">
  </script>

  <script type="text/javascript" src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.js">
  </script>
</head>

<body>
  <script type="text/javascript">
    // Specifying some arrays
    var a = [2, 4, 6, 8];
    var b = [1, 3, 5, 7];

    // Calling multiplyTransformMatrices() function over
    // the above specified arrays
    console.log(fabric.util.multiplyTransformMatrices(a, b, true));
    console.log(fabric.util.multiplyTransformMatrices(a, b, false));
  </script>
</body>

</html>
```

**输出:**

```
[20,28,52,76,0,0]
[20,28,52,76,null,null]
```