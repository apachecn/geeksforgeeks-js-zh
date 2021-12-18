# D3.js | d3.cross()功能

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-cross-function/](https://www.geeksforgeeks.org/d3-js-d3-cross-function/)

D3.js 中的 **d3.cross()函数**用于返回给定的两个数组 **A** 和 **B** 的笛卡尔乘积。

**语法:**

```
d3.cross(Array1, Array2)
```

**参数:**该功能接受上面提到的和下面描述的两个参数:

*   **Array1:** 这是第一个数组，其元素将与 array2 进行笛卡尔乘积运算。
*   **Array2:** 这是第二个数组，其元素将与 array1 进行笛卡尔乘积运算。

**返回值:**返回两个给定数组中每个数组的两个元素的笛卡儿积数组。

以下程序说明了 D3.js.
**中的 **d3.cross()** 功能示例 1:**

```
<html>

<head>
    <title>
      Getting cartesian product
      of the two given array
  </title>
</head>

<body>
    <script src='https://d3js.org/d3.v4.min.js'>
  </script>

    <script>
        // initialising the array of elements
        var Array1 = [10, 20, 30];
        var Array2 = [1, 2, 3];

        // Calling to d3.cross() function
        A = d3.cross(Array1, Array2);

        // Getting cartesian product of the two given array
        document.write(A + "<br>");
    </script>
</body>

</html>
```

**输出:**

```
[[10, 1], [10, 2], [10, 3], [20, 1], [20, 2], [20, 3], [30, 1], [30, 2], [30, 3]]
```

**例 2:**

```
<html>

<head>
    <title>
      Getting cartesian product 
      of the two given array
  </title>
</head>

<body>
    <script src='https://d3js.org/d3.v4.min.js'>
  </script>

    <script>
        // initialising the array of elements
        var Array1 = ["A", "B", "C"];
        var Array2 = ["a", "b", "c"];

        // Calling to d3.cross() function
        A = d3.cross(Array1, Array2);

        // Getting cartesian product of the two given array
        document.write(A + "<br>");
    </script>
</body>

</html>
```

**输出:**

```
[[A, a], [A, b], [A, c], [B, a], [B, b], [B, c], [C, a], [C, b], [C, c]]
```

**参考:**T2】https://devdocs.io/d3~4/d3-array#cross