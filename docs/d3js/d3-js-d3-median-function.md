# D3.js | d3 .中位数()函数

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-median-function/](https://www.geeksforgeeks.org/d3-js-d3-median-function/)

D3.js 中的 **d3 .中值()函数**用于返回给定数组元素的中值或中点。如果数组为空，则返回 undefined。

**语法:**

```
d3.median(Array)
```

**参数:**该函数接受一个参数**数组**，它是一个元素数组，其中值将被计算。这里的元素应该是整数而不是字符串，否则会返回 undefined。

**返回值:**返回给定数组元素的中值。

下面的程序说明了 D3.js.
**中的 **d3 .中位数()**函数示例 1:**

```
<html>

<head>
    <title>
      Getting median of the 
      elements of given array
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

        // Calling to d3.median() function
        A = d3.median(Array1);
        B = d3.median(Array2);
        C = d3.median(Array3);
        D = d3.median(Array4);

        // Getting median of the given array's element
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
35
1.5
1.5
0.08
```

**例 2:**

```
<html>

<head>
    <title>
      Getting median of the 
      elements of given array
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
        var Array4 = ["Geek", "Geeks", 2, 3, 6, "GeeksforGeeks"];

        // Calling to d3.median() function
        A = d3.median(Array1);
        B = d3.median(Array2);
        C = d3.median(Array3);
        D = d3.median(Array4);

        // Getting median of the given array's element
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
1
3
```

**注意:**在上面的输出中，如果参数为空或字符串，则返回 undefined，如果参数为包含一些整数值的字符串，则返回整数值的中值。

**参考:**T2】https://devdocs.io/d3~4/d3-array#median