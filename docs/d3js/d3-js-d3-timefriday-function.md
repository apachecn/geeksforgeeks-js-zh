# D3 . js | D3 . time 星期五功能

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-timefriday-function/](https://www.geeksforgeeks.org/d3-js-d3-timefriday-function/)

D3.js 中的 **d3.timeFriday 函数**用于返回给定起止日期范围内基于星期五的所有日期。

**语法:**

```
d3.timeFriday.range( start, end, step );
```

**参数:**该函数接受下面给出的三个参数:

*   **Start:** This parameter saves the given start date.
*   **End:** This parameter saves the given end date.
*   **Step:** is an optional parameter to save the value for skipping the date.

**返回值:**该函数返回基于周五的所有日期。

以下程序说明了 D3.js 中的 **d3.timeFriday** 功能:

**例 1:**

```
<!DOCTYPE html>
<html>

<head>
    <title>
        D3.js | d3.timeFriday Function
    </title>

    <script src = 
        "https://d3js.org/d3.v4.min.js">
    </script>
</head>

<body>
    <script>

        // Initialising start and end date
        var start = new Date(2015, 07, 01);
        var end = new Date(2015, 07, 30);

        // Calling the timeFriday function
        // without step value
        var a = d3.timeFriday.range(start, end);

        // Getting the friday dates
        console.log(a);
    </script>
</body>

</html>
```

**输出:**

```
["2015-08-06T18:30:00.000Z", "2015-08-13T18:30:00.000Z", 
"2015-08-20T18:30:00.000Z", "2015-08-27T18:30:00.000Z"]

```

**例 2:**

```
<!DOCTYPE html>
<html>

<head>
    <title>
        D3.js | d3.timeFriday Function
    </title>

    <script src = 
        "https://d3js.org/d3.v4.min.js">
    </script>
</head>

<body>
    <script>

        // Initialising start and end date
        var start = new Date(2015, 07, 01);
        var end = new Date(2015, 07, 30);

        // Calling the timeFriday function
        // with step value
        var a = d3.timeFriday.range(start, end, 2);

        // Getting the friday dates
        console.log(a);
    </script>
</body>

</html>
```

**输出:**

```
["2015-08-06T18:30:00.000Z", "2015-08-20T18:30:00.000Z"]

```

**参考:**T2】https://devdocs.io/d3~5/d3-time#timeFriday