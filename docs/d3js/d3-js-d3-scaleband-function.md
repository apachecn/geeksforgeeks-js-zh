# D3.js | d3.scaleBand()函数

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-scaleband-function/](https://www.geeksforgeeks.org/d3-js-d3-scaleband-function/)

D3.js 中的 **d3.scaleBand()函数**用于构造一个新的波段尺度，其域指定为一组值，范围为波段的最小和最大范围。此函数将范围分成 n 个波段，其中 n 是域数组中的值的数量。

**语法:**

```
d3.scaleBand().domain(array of values).range(array of values);
```

**参数:**此功能不接受任何参数。

**返回值:**该函数返回域值的对应范围。

下面的程序说明了 D3.js 中的 **d3.scaleBand()** 功能:

**例 1:**

```
<!DOCTYPE html>
<html>

<head>
    <title>
        D3.js | d3.scaleBand() Function
    </title>

    <script src =
        "https://d3js.org/d3.v4.min.js">
    </script>
</head>

<body>
    <script>

        // Calling the scaleBand() function
        var A = d3.scaleBand()
            .domain(['January', 'February', 'March', 'April', 'May'])
            .range([10, 50]);

        // Getting the corresponding range for
        // the domain value
        console.log(A('January'));
        console.log(A('February'));
        console.log(A('March'));
        console.log(A('April'));
        console.log(A('May'));
    </script>
</body>

</html>
```

**输出:**

```
10
18
26
34
42

```

**例 2:**

```
<!DOCTYPE html>
<html>

<head>
    <title>
        D3.js | d3.scaleBand() Function
    </title>

    <script src =
        "https://d3js.org/d3.v4.min.js">
    </script>
</head>

<body>
    <script>

        // Calling the scaleBand() function
        var A = d3.scaleBand()
            .domain(['January', 'February', 'March', 'April', 'May'])
            .range([1, 2]);

        // Getting the corresponding range for
        // the domain value
        console.log(A('January'));
        console.log(A('February'));
        console.log(A('March'));
        console.log(A('April'));
        console.log(A('May'));
    </script>
</body>

</html>
```

**输出:**

```
1
1.2
1.4
1.6
1.8

```

**参考:**T2】https://devdocs.io/d3~5/d3-scale#scaleBand