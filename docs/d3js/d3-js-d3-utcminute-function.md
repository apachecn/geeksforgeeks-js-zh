# D3 . js | D3 . utc 分钟功能

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-utcminute-function/](https://www.geeksforgeeks.org/d3-js-d3-utcminute-function/)

D3.js 中的**D3 . UTC 分钟功能**用于返回以分钟为单位的所有时间，日期在协调世界时(UTC)中给定的开始和结束时间范围内。

**语法:**

```
d3.utcMinute.range( start, end, step );
```

**参数:**该函数接受下面给出的三个参数:

*   **Start:** This parameter stores the given start time.
*   **End:** This parameter saves the given end time.
*   **Step:** is an optional parameter to save the value for skipping minutes.

**返回值:**该函数返回给定范围内所有可能的分钟数。

下面的程序说明了 D3.js 中的**D3 . utc 分钟**功能:

**例 1:**

```
<!DOCTYPE html>
<html>

<head>
    <title>
        D3.js | d3.utcMinute Function
    </title>

    <script src = 
        "https://d3js.org/d3.v4.min.js">
    </script>
</head>

<body>
    <script>

        // Initialising start and end time
        var start = new Date(2015, 07, 01, 4, 10);
        var end = new Date(2015, 07, 01, 4, 15);

        // Calling the utcMinute function
        // without step value
        var a = d3.utcMinute.range(start, end);

        // Getting the minute values
        console.log(a);
    </script>
</body>

</html>    
```

**输出:**

```
["2015-07-31T22:40:00.000Z", "2015-07-31T22:41:00.000Z", "2015-07-31T22:42:00.000Z",
"2015-07-31T22:43:00.000Z", "2015-07-31T22:44:00.000Z"]

```

**例 2:**

```
<!DOCTYPE html>
<html>

<head>
    <title>
        D3.js | d3.utcMinute Function
    </title>

    <script src = 
        "https://d3js.org/d3.v4.min.js">
    </script>
</head>

<body>
    <script>

        // Initialising start and end time
        var start = new Date(2015, 07, 01, 4, 10);
        var end = new Date(2015, 07, 01, 4, 15);

        // Calling the utcMinute function
        // with step value
        var a = d3.utcMinute.range(start, end, 2);

        // Getting the minute values
        console.log(a);
    </script>
</body>

</html>
```

**输出:**

```
["2015-07-31T22:40:00.000Z", "2015-07-31T22:42:00.000Z", "2015-07-31T22:44:00.000Z"]

```

**参考:**T2】https://devdocs.io/d3~5/d3-time#timeMinute