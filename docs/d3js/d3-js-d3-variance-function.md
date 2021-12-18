# D3 . js | D3 . variation()函数

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-variance-function/](https://www.geeksforgeeks.org/d3-js-d3-variance-function/)

D3.js 中的 **d3.variance()函数**用于返回给定数组元素的方差。如果数组少于两个元素，则返回 undefined。

**语法:**

```
d3.variance(Array)
```

**参数:**这个函数接受一个参数**数组**，它是一个要计算方差的元素数组。这里的元素应该是整数而不是字符串，否则会返回 undefined。

**返回值:**返回给定数组元素的方差。

以下程序说明了 D3.js.
**中的**D3 . variation()**功能示例 1:**

```
<html>

<head>
    <title>
      Getting variance of
      the elements of given array
  </title>
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

        // Calling to d3.variance() function
        A = d3.variance(Array1);
        B = d3.variance(Array2);
        C = d3.variance(Array3);
        D = d3.variance(Array4);

        // Getting variance of the given array's element
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
350
0.5
12.763333333333332
0.19180800000000003
```

**例 2:**

```
<html>

<head>
    <title>
      Getting variance of the
      elements of given array
  </title>
</head>

<body>
    <script src='https://d3js.org/d3.v4.min.js'>
  </script>

    <script>
        // initialising the array of elements
        var Array1 = [1];
        var Array2 = ["a", "b", "c"];
        var Array3 = [1, 2, "B", "C"];
        var Array4 = ["Geek", "Geeks", 2, 3, "GeeksforGeeks"];

        // Calling to d3.variance() function
        A = d3.variance(Array1);
        B = d3.variance(Array2);
        C = d3.variance(Array3);
        D = d3.variance(Array4);

        // Getting variance of the given array's element
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
undefined
0.5
0.5
```

**注意:**在上面的输出中，如果参数的元素或字符串少于一个，则返回 undefined，如果参数的字符串包含一些整数值，则返回整数值的方差。

**参考:**T2】https://devdocs.io/d3~4/d3-array#variance