# D3.js | d3 .升序()函数

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-ascending-function/](https://www.geeksforgeeks.org/d3-js-d3-ascending-function/)

D3.js 中的 **d3 .升序()函数**是一个内置的自然顺序比较器函数，它接受两个参数并计算它们的自然顺序。

**语法:**

```
d3.ascending(x, y)
```

**参数:**这个函数接受两个参数 x，y，需要计算它们的自然阶。

**返回值:**函数有以下返回值:

*   如果两个值按**升序排列**，则返回 **-1** 。
*   如果两个值按**降序排列**，则返回 **1** 。
*   如果两个值**相等**，则返回 **0**
*   如果没有可比较的值，即只有一个或没有参数传递给函数，则返回 **NaN** 。

下面的程序说明了 D3.js 中的 **d3 .升序()**功能。

**例 1:**

```
<!DOCTYPE html>
<html>

<head>
    <title>D3.js | d3.ascending() function</title>

    <script src='https://d3js.org/d3.v4.min.js'></script>
</head>

<body>
    <script>
        // If the two values are in 
        // ascending order
        document.write(d3.ascending(33, 64) + "<br>"); // -1

        // If the two values are in 
        // descending order
        document.write(d3.ascending(42, 24) + "<br>"); // 1

        // If the two values are equal
        document.write(d3.ascending(43, 43) + "<br>"); // 0
    </script>
</body>

</html>
```

**输出:**

```
-1
1
0

```

**例 2:**

```
<!DOCTYPE html>
<html>

<head>
    <title>D3.js d3.ascending() function</title>

    <script src='https://d3js.org/d3.v4.min.js'></script>
</head>

<body>
    <script>
        // If no values are passed
        document.write(d3.ascending() + "<br>"); // NaN

        // If only one value is passed
        document.write(d3.ascending(42) + "<br>"); // NaN

        // If the two values are equal
        document.write(d3.ascending("x", "x") + "<br>"); // 0

        // If the two values are in
        // ascending order
        document.write(d3.ascending("x", "y") + "<br>"); // -1

        // If the two values are in
        // descending order
        document.write(d3.ascending("y", "x") + "<br>"); // 1
    </script>
</body>

</html>
```

**输出:**

```
NaN
NaN
0
-1
1

```

**参考:**T2】https://devdocs.io/d3~5/d3-array#ascending