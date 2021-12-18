# D3 . js | D3 . utc 星期五功能

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-utcfriday-function/](https://www.geeksforgeeks.org/d3-js-d3-utcfriday-function/)

D3.js 中的 **d3.utcFriday 函数**用于返回协调世界时(UTC)中给定的开始和结束日期范围内基于星期五的所有日期。

**语法:**

```
d3.utcFriday.range( start, end, step );
```

**参数:**该函数接受下面给出的三个参数:

*   **Start:** This parameter saves the given start date.
*   **End:** This parameter saves the given end date.
*   **Step:** is an optional parameter, which is used to skip the date.

**返回值:**该函数返回基于周五的所有日期。

下面的程序说明了 D3.js 中的 **d3.utcFriday** 功能:

**例 1:**

```
<!DOCTYPE html>
<html>

<head>
    <title>
        D3.js | d3.utcFriday Function
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

        // Calling the utcFriday function
        // without step value
        var a = d3.utcFriday.range(start, end);

        // Getting the friday dates
        console.log(a);
    </script>
</body>

</html>    
```

**输出:**

```
["2015-08-07T00:00:00.000Z", "2015-08-14T00:00:00.000Z", 
"2015-08-21T00:00:00.000Z", "2015-08-28T00:00:00.000Z"]

```

**例 2:**

```
<!DOCTYPE html>
<html>

<head>
    <title>
        D3.js | d3.utcFriday Function
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

        // Calling the utcFriday function
        // with step value
        var a = d3.utcFriday.range(start, end, 2);

        // Getting the friday dates
        console.log(a);
    </script>
</body>

</html>                    
```

**输出:**

```
["2015-08-07T00:00:00.000Z", "2015-08-21T00:00:00.000Z"]

```

**参考:**T2】https://devdocs.io/d3~5/d3-time#timeFriday