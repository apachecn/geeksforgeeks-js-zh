# D3.js | d3.utcSeconds()功能

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-utcseconds-function/](https://www.geeksforgeeks.org/d3-js-d3-utcseconds-function/)

D3.js 中的 **d3.utcSeconds()函数**用于返回在协调世界时(UTC)中给定的开始和结束时间范围内所有带有日期的秒。

**语法:**

```
d3.utcSeconds( start, end, step );
```

**参数:**该函数接受下面给出的三个参数:

*   **Start:** This parameter stores the given start time.
*   **End:** This parameter saves the given end time.
*   **Step:** is an optional parameter to save the value for skipping seconds.

**返回值:**该函数返回给定范围内所有可能的秒数。

下面的程序说明了 D3.js 中的 **d3.utcSeconds()** 功能:

**例 1:**

```
<!DOCTYPE html>
<html>

<head>
    <title>
        D3.js | d3.utcSeconds() Function
    </title>

    <script src = 
        "https://d3js.org/d3.v4.min.js">
    </script>
</head>

<body>
    <script>

        // Initialising start and end time
        var start = new Date(2015, 07, 01, 4, 10, 10);
        var end = new Date(2015, 07, 01, 4, 10, 15);

        // Calling the utcSeconds() function
        // without step value
        var a = d3.utcSeconds(start, end);

        // Getting the seconds values
        console.log(a);
    </script>
</body>

</html>
```

**输出:**

```
["2015-07-31T22:40:10.000Z", "2015-07-31T22:40:11.000Z", "2015-07-31T22:40:12.000Z", 
"2015-07-31T22:40:13.000Z", "2015-07-31T22:40:14.000Z"]

```

**例 2:**

```
<!DOCTYPE html>
<html>

<head>
    <title>
        D3.js | d3.utcSeconds() Function
    </title>

    <script src = 
        "https://d3js.org/d3.v4.min.js">
    </script>
</head>

<body>
    <script>

        // Initialising start and end time
        var start = new Date(2015, 07, 01, 4, 10, 10);
        var end = new Date(2015, 07, 01, 4, 10, 15);

        // Calling the utcSeconds() function
        // with step value
        var a = d3.utcSeconds(start, end, 2);

        // Getting the seconds values
        console.log(a);
    </script>
</body>

</html>
```

**输出:**

```
["2015-07-31T22:40:10.000Z", "2015-07-31T22:40:12.000Z", "2015-07-31T22:40:14.000Z"]

```

**参考:**T2】https://devdocs.io/d3~5/d3-time#timeSeconds