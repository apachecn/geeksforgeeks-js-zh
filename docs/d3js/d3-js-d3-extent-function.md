# D3 . js | D3 . extend()函数

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-extent-function/](https://www.geeksforgeeks.org/d3-js-d3-extent-function/)

D3.js 中的 **d3.extent()函数**用于使用自然顺序返回给定数组中的最小值和最大值。如果一个数组是空的，那么它返回 undefined，undefined 作为输出。

**语法:**

```
d3.extent(Array)
```

**参数:**这个函数接受一个参数**数组**，它是一个元素数组，数组中的最小值和最大值都要计算。这里的元素可以是整数或任何字符串。

**返回值:**从给定数组中返回数组中的最小值和最大值。

下面的程序说明了 D3.js 中的 **d3.extent()** 功能。

**例 1:**

```
<html>

<head>
    <title>
      Getting minimum and 
      maximum value in an array
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

        // Calling to d3.extent() function
        A = d3.extent(Array1);
        B = d3.extent(Array2);
        C = d3.extent(Array3);
        D = d3.extent(Array4);

        // Getting minimum and maximum value
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
10, 60
1, 2
0, 6.8
0.008, 0.8
```

**例 2:**

```
<html>

<head>
    <title>
      Getting minimum 
      and maximum value
  </title>
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

        // Calling to d3.extent() function
        A = d3.extent(Array1);
        B = d3.extent(Array2);
        C = d3.extent(Array3);
        D = d3.extent(Array4);

        // Getting minimum and maximum value
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
undefined, undefined
a, c
A, C
Geek, GeeksforGeeks
```

**注:**在上述输出中，第一个元素为最小值，第二个元素为最大值。

**参考:**T2】https://devdocs.io/d3~4/d3-array#extent