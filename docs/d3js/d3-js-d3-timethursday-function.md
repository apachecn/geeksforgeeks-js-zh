# D3.js | d3.timeThursday 功能

> 原文:[https://www . geesforgeks . org/D3-js-D3-time Thursday-function/](https://www.geeksforgeeks.org/d3-js-d3-timethursday-function/)

D3.js 中的 **d3.timeThursday 函数**用于返回给定起止日期范围内基于周四的所有日期。

**语法:**

```
d3.timeThursday.range( start, end, step );
```

**参数:**该函数接受下面给出的三个参数:

*   **Start:** This parameter saves the given start date.
*   **End:** This parameter saves the given end date.
*   **Step:** is an optional parameter to save the value for skipping the date.

**返回值:**该函数返回基于周四的所有日期。

下面的程序说明了 D3.js 中的 **d3.timeThursday** 功能:

**例 1:**

```
<!DOCTYPE html>
<html>

<head>
    <title>
        D3.js | d3.timeThursday Function
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

        // Calling the timeThursday function
        // without step value
        var a = d3.timeThursday.range(start, end);

        // Getting the Thursday dates
        console.log(a);
    </script>
</body>

</html>
```

**输出:**

```
["2015-08-05T18:30:00.000Z", "2015-08-12T18:30:00.000Z", 
"2015-08-19T18:30:00.000Z", "2015-08-26T18:30:00.000Z"]

```

**例 2:**

```
<!DOCTYPE html>
<html>

<head>
    <title>
        D3.js | d3.timeThursday Function
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

         // Calling the timeThursday function
         // with step value
         var a = d3.timeThursday.range(start, end, 2);

         // Getting the Thursday dates
         console.log(a);
    </script>
</body>

</html>
```

**输出:**

```
["2015-08-05T18:30:00.000Z", "2015-08-19T18:30:00.000Z"]

```

**参考:**T2】https://devdocs.io/d3~5/d3-time#timeThursday