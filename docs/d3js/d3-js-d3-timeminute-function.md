# D3.js | d3.timeMinute 功能

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-timeminute-function/](https://www.geeksforgeeks.org/d3-js-d3-timeminute-function/)

D3.js 中的 **d3.timeMinute 功能**用于返回在给定的开始和结束时间范围内的所有时间，以分钟为单位。

**语法:**

```
d3.timeMinute.range( start, end, step );
```

**参数:**该函数接受下面给出的三个参数:

*   **Start:** This parameter stores the given start time.
*   **End:** This parameter saves the given end time.
*   **Step:** is an optional parameter to save the value for skipping minutes.

**返回值:**该函数返回给定范围内所有可能的分钟数。

以下程序说明了 D3.js 中的 **d3.timeMinute** 功能:

**例 1:**

```
<!DOCTYPE html>
<html>

<head>
    <title>
        D3.js | d3.timeMinute Function
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

        // Calling the timeMinute function
        // without step value
        var a = d3.timeMinute.range(start, end);

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
        D3.js | d3.timeMinute Function
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

        // Calling the timeMinute function
        // with step value
        var a = d3.timeMinute.range(start, end, 2);

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