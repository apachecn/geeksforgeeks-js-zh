# D3.js | d3.min()功能

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-min-function/](https://www.geeksforgeeks.org/d3-js-d3-min-function/)

D3.js 中的 **d3.min()函数**用于*使用自然顺序*返回给定数组中的最小值。如果一个数组是空的，那么它作为输出返回 undefined。

**语法:**

```
d3.min(Array)
```

**参数:**这个函数接受一个参数**数组**，它是一个元素数组，其最小值将被计算。这里的元素可以是整数或任何字符串。

**返回值:**返回最小值。

下面的程序说明了 D3.js 中的 d3.min()函数。

**例 1:**

```
<html>

<head>
    <title>Getting minimum value</title>
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

        // Calling to d3.min() function
        A = d3.min(Array1);
        B = d3.min(Array2);
        C = d3.min(Array3);
        D = d3.min(Array4);

        // Getting minimum value
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
10
1
0
0.008
```

**例 2:**

```
<html>

<head>
    <title>Getting minimum value</title>
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

        // Calling to d3.min() function
        A = d3.min(Array1);
        B = d3.min(Array2);
        C = d3.min(Array3);
        D = d3.min(Array4);

        // Getting minimum value
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
a
A
Geek
```