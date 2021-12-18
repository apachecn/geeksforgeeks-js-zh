# D3 . js | D3 . timed day 功能

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-timesunday-function/](https://www.geeksforgeeks.org/d3-js-d3-timesunday-function/)

D3.js 中的**D3 . time date 函数**用于返回给定起止日期范围内基于周日的所有日期。

**语法:**

```
d3.timeSunday.range(start, end, step);
```

**参数:**该函数接受三个参数，如下所示:

*   **开始:**这是给定的开始日期。
*   **结束:**这是给定的结束日期。
*   **步骤:**这是用于跳过日期的可选值。

**返回值:**该函数返回基于周日的所有日期。

下面的程序说明了 D3.js 中的**D3 . timed day**功能:
T3】例 1:

```
<!DOCTYPE html>
<html>

<head>
    <title>
        D3.js | d3.timeSunday Function
    </title>

    <script src=
        "https://d3js.org/d3.v4.min.js">
    </script>
</head>

<body>
    <script>

        // Initialising start and end date
        var start = new Date(2015, 07, 01);
        var end = new Date(2015, 07, 30);

        // Calling the timeSunday function
        // without step value
        var a = d3.timeSunday.range(start, end);

        // Getting the Sunday dates
        console.log(a);
    </script>
</body>

</html>    
```

**输出:**

> 【“2015-08-01t 18:30:00.000 z”“2015-08-08t 18:30:00.000 z”“2015-08-15t 18:30:00.000 z”“2015-08-22t 18:30:00.000 z”】

**例 2:**

```
<!DOCTYPE html>
<html>

<head>
    <title>
        D3.js | d3.timeSunday Function
    </title>

    <script src=
        "https://d3js.org/d3.v4.min.js">
    </script>
</head>

<body>
    <script>

        // Initialising start and end date
        var start = new Date(2015, 07, 01);
        var end = new Date(2015, 07, 30);

        // Calling the timeSunday function
        // with step value
        var a = d3.timeSunday.range(start, end, 2);

        // Getting the Sunday dates
        console.log(a);
    </script>
</body>

</html>    
```

**输出:**

```
["2015-08-01T18:30:00.000Z", "2015-08-15T18:30:00.000Z"]

```

**参考:**T2】https://devdocs.io/d3~5/d3-time#timeSunday