# D3.js | d3.pairs()功能

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-pairs-function/](https://www.geeksforgeeks.org/d3-js-d3-pairs-function/)

D3.js 中的 **d3.pairs()函数**用于根据给定的数组元素创建一对数组元素。如果给定数组的元素少于两个，则返回空数组。

**语法:**

```
d3.pairs(Array)
```

**参数:**该函数接受一个参数**数组**，其元素将被配对。

**返回值:**返回成对元素的数组。

下面的程序说明了 D3.js 中的 **d3.pairs()** 功能。

**例 1:**

```
<html>

<head>
    <title>
      Getting pair of two elements 
      from the elements of given array
  </title>
</head>

<body>
    <script src='https://d3js.org/d3.v4.min.js'>
  </script>

    <script>
        // initialising the arrays of elements
        var Array1 = [10, 20, 30, 40];
        var Array2 = [1, 2, 3, 4];

        // Calling to d3.pairs() function
        A = d3.pairs(Array1);
        B = d3.pairs(Array2);

        // Getting pair of two elements from 
        // the elements of given array
        document.write(A + "<br>");
        document.write(B + "<br>");
    </script>
</body>

</html>
```

**输出:**

```
[[10, 20], [20, 30], [30, 40]]
[[1, 2], [2, 3], [3, 4]]
```

**例 2:**

```
<html>

<head>
    <title>
      Getting pair of two elements
      from the elements of given array
  </title>
</head>

<body>
    <script src='https://d3js.org/d3.v4.min.js'>
  </script>

    <script>
        // initialising the arrays of elements
        var Array1 = ["A", "B", "C"];
        var Array2 = ["a", "b"];

        // Calling to d3.pairs() function
        A = d3.pairs(Array1);
        B = d3.pairs(Array2);

        // Getting pair of two elements from
        // the elements of given array
        document.write(A + "<br>");
        document.write(B + "<br>");
    </script>
</body>

</html>
```

**输出:**

```
[[A, B], [B, C]]
[a, b]
```