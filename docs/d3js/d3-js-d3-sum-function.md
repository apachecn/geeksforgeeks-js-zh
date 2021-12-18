# D3.js | d3.sum()函数

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-sum-function/](https://www.geeksforgeeks.org/d3-js-d3-sum-function/)

D3.js 中的 **d3.sum()函数**用于返回给定数组元素的和。如果数组为空，则返回 0。

**语法:**

```
d3.sum(Array)
```

**参数:**这个函数接受一个参数**数组**，它是一个元素数组，元素的和要被计算。

**返回值:**返回给定数组元素的和。

下面的程序说明了 D3.js 中的 **d3.sum()** 函数。

**例 1:**

```
<html>

<head>
    <title>
      Getting sum of the elements of given array
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

        // Calling to d3.sum() function
        A = d3.sum(Array1);
        B = d3.sum(Array2);
        C = d3.sum(Array3);
        D = d3.sum(Array4);

        // Getting sum of the given array's element
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
210
3
8.3
0.888
```

**例 2:**

```
<html>

<head>
    <title>
      Getting sum of the elements of given array
  </title>
</head>

<body>
    <script src='https://d3js.org/d3.v4.min.js'>
  </script>

    <script>
        // initialising the array of elements
        var Array1 = [];
        var Array2 = ["a", "b", "c"];
        var Array3 = [1, "B", "C"];
        var Array4 = ["Geek", "Geeks", 2, 3, "GeeksforGeeks"];

        // Calling to d3.sum() function
        A = d3.sum(Array1);
        B = d3.sum(Array2);
        C = d3.sum(Array3);
        D = d3.sum(Array4);

        // Getting sum of the given array's element
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
0
0
1
5
```

**注意:**在上面的输出中，如果参数为空或字符串，则返回 0，如果参数为包含一些整数值的字符串，则返回整数值的总和。

**参考:t1】[https://devdocs . io/D3 ~ 4/D3 阵列#sum](https://devdocs.io/d3~4/d3-array#sum)**