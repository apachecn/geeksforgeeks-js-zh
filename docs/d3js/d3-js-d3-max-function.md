# D3.js | d3.max()功能

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-max-function/](https://www.geeksforgeeks.org/d3-js-d3-max-function/)

D3.js 中的 **d3.max()函数**用于使用自然顺序返回给定数组中的最大值。如果一个数组是空的，那么它作为输出返回 undefined。

**语法:**

```
d3.max(Array)
```

**参数:**该函数接受一个参数**数组**，它是一个元素数组，其最大值将被计算。这里的元素可以是整数或任何字符串。

**返回值:**返回最大值。

以下程序说明了 D3.js.
**中的 **d3.max()** 功能示例 1:**

```
<html>

<head>
    <title>Getting maximum value</title>
</head>

<body>
    <script src='https://d3js.org/d3.v4.min.js'>
  </script>

    <script>
        // initialising the array of elements
        var Array1 = [10, 20, 30, 40, 50, 60];
        var Array2 = [1, 2];
        var Array3 = [0, 1.5, 6.8];
        var Array4 = [.8, .08, .008];

        // Calling to d3.max() function
        A = d3.max(Array1);
        B = d3.max(Array2);
        C = d3.max(Array3);
        D = d3.max(Array4);

        // Getting maximum value
        document.write(A + "<br>");
        document.write(B + "<br>");
        document.write(C + "<br>");
        document.write(D + "<br>");
    </script>
</body>

</html>
```

**输出:**

```
60
2
6.8
0.8
```

**例 2:**

```
<html>

<head>
    <title>Getting maximum value</title>
</head>

<body>
    <script src='https://d3js.org/d3.v4.min.js'>
  </script>

    <script>
        // initialising the array of elements
        var Array1 = [];
        var Array2 = ["a", "b", "c"];
        var Array3 = ["A", "B", "C"];
        var Array4 = ["Geek", "Geeks", "GeeksforGeeks"];

        // Calling to d3.max() function
        A = d3.max(Array1);
        B = d3.max(Array2);
        C = d3.max(Array3);
        D = d3.max(Array4);

        // Getting maximum value
        document.write(A + "<br>");
        document.write(B + "<br>");
        document.write(C + "<br>");
        document.write(D + "<br>");
    </script>
</body>

</html>
```

**输出:**

```
undefined
c
C
GeeksforGeeks
```