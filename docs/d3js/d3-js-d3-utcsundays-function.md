# D3 . js | D3 . utchnys()功能

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-utcsundays-function/](https://www.geeksforgeeks.org/d3-js-d3-utcsundays-function/)

D3.js 中的**D3 . utchnys()函数**用于返回协调世界时(UTC)中给定的开始和结束日期范围内基于星期日的所有日期。

**语法:**

```
d3.utcSundays( start, end, step );
```

**参数:**该函数接受下面给出的三个参数:

*   **Start:** This parameter saves the given start date.
*   **End:** This parameter saves the given end date.
*   **Step:** is an optional parameter to save the value for skipping the date.

**返回值:**该函数返回基于周日的所有日期。

下面的程序说明了 D3.js 中的 **d3.utcSundays()** 功能:

**例 1:**

```
<!DOCTYPE html>
<html>

<head>
    <title>
        D3.js | d3.utcSundays() Function
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

        // Calling the utcSundays() function
        // without step value
        var a = d3.utcSundays(start, end);

        // Getting the Sunday dates
        console.log(a);
    </script>
</body>

</html>    
```

**输出:**

```
["2015-08-02T00:00:00.000Z", "2015-08-09T00:00:00.000Z", 
"2015-08-16T00:00:00.000Z", "2015-08-23T00:00:00.000Z"]

```

**例 2:**

```
<!DOCTYPE html>
<html>

<head>
    <title>
        D3.js | d3.utcSundays() Function
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

        // Calling the utcSundays() function
        // with step value
        var a = d3.utcSundays(start, end, 2);

        // Getting the Sunday dates
        console.log(a);
    </script>
</body>

</html>    
```

**输出:**

```
["2015-08-02T00:00:00.000Z", "2015-08-16T00:00:00.000Z"]

```

**参考:**T2】https://devdocs.io/d3~5/d3-time#timeSundays