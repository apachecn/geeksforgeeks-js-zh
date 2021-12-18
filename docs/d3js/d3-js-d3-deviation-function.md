# D3.js | d3 .偏差()功能

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-deviation-function/](https://www.geeksforgeeks.org/d3-js-d3-deviation-function/)

D3.js 中的 **d3.deviation()函数**用于返回给定数组元素的标准差。如果数组少于两个元素，则返回 undefined。

**语法:**

```
d3.deviation(Array)
```

**参数:**这个函数接受一个参数**数组**，它是一个要计算标准差的元素数组。这里的元素应该是整数而不是字符串，否则会返回 undefined。

**返回值:**返回给定数组元素的标准差。

下面的程序说明了 D3.js.
**中的 **d3.deviation()** 功能示例 1:**

```
<html>

<head>
    <title>
      Getting standard deviation of 
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

        // Calling to d3.deviation() function
        A = d3.deviation(Array1);
        B = d3.deviation(Array2);
        C = d3.deviation(Array3);
        D = d3.deviation(Array4);

        // Getting standard deviation of the given array's element
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
18.708286933869708
0.7071067811865476
3.572580766523457
0.4379589021814719
```

**例 2:**

```
<html>

<head>
    <title>
      Getting standard deviation
      of the elements of given array
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

        // Calling to d3.deviation() function
        A = d3.deviation(Array1);
        B = d3.deviation(Array2);
        C = d3.deviation(Array3);
        D = d3.deviation(Array4);

        // Getting standard deviation of
        // the given array's element
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
0.7071067811865476
0.7071067811865476
```

**注意:**在上面的输出中，如果参数的元素或字符串少于一个，则返回 undefined，如果参数的字符串包含一些整数值，则返回整数值的标准偏差。

**参考:**T2】https://devdocs.io/d3~4/d3-array#deviation