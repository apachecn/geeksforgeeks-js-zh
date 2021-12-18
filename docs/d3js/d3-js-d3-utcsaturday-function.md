# D3 . js | D3 . utc 星期六功能

> 原文:[https://www . geesforgeks . org/D3-js-D3-utc 星期六-function/](https://www.geeksforgeeks.org/d3-js-d3-utcsaturday-function/)

D3.js 中的**D3 . UTC 星期六功能**用于返回给定的开始和结束日期协调世界时(UTC)范围内基于星期六的所有日期。

**语法:**

```
d3.utcSaturday.range(start, end, step);
```

**参数:**该功能接受以下给出的三个参数:

*   **Start:** This is the given start date.
*   **End:** This is the given end date.
*   **Step:** This is an optional value for skipping the date.

**返回值:**该函数返回基于周六的所有日期。

下面的程序说明了 D3.js 中的**D3 . utcstry**功能:

**例 1:**

```
<!DOCTYPE html>
<html>

<head>
    <title>
        D3.js | d3.utcSaturday Function
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

        // Calling the utcSaturday function
        // without step value
        var a = d3.utcSaturday.range(start, end);

        // Getting the Saturday dates
        console.log(a);
    </script>
</body>

</html>    
```

**产量:**

> 【“2015-08-01t 00:00:00.000 z”“2015-08-08t 00:00:00.000 z”“2015-08-15t 00:00:00.000 z”“2015-08-22t 00:00:00.000 z”“2015-08-29t 00:00

**例 2:**

```
<!DOCTYPE html>
<html>

<head>
    <title>
        D3.js | d3.utcSaturday Function
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

        // Calling the utcSaturday function
        // with step value
        var a = d3.utcSaturday.range(start, end, 2);

        // Getting the Saturday dates
        console.log(a);
    </script>
</body>

</html>    
```

**输出:**

```
["2015-08-01T00:00:00.000Z", "2015-08-15T00:00:00.000Z", "2015-08-29T00:00:00.000Z"]

```

**参考:**T2】https://devdocs.io/d3~5/d3-time#timeSaturday