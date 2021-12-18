# D3 . js | D3 . timestaurday 函数

> 原文:[https://www . geesforgeks . org/D3-js-D3-times aturday-function/](https://www.geeksforgeeks.org/d3-js-d3-timesaturday-function/)

D3.js 中的**D3 . time staturday 函数**用于返回给定起止日期范围内基于周六的所有日期。

**语法:**

```
d3.timeSaturday.range( start, end, step );
```

**参数:**该函数接受下面给出的三个参数:

*   **Start:** This parameter saves the given start date.
*   **End:** This parameter saves the given end date.
*   **Step:** is an optional parameter to save the value for skipping the date.

**返回值:**该函数返回基于周六的所有日期。

下面的程序说明了 D3.js 中的**D3 . time staturday**功能:

**例 1:**

```
<!DOCTYPE html>
<html>

<head>
    <title>
        D3.js | d3.timeSaturday Function
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

        // Calling the timeSaturday function
        // without step value
        var a = d3.timeSaturday.range(start, end);

        // Getting the Saturday dates
        console.log(a);
    </script>
</body>

</html>    
```

**输出:**

```
["2015-07-31T18:30:00.000Z", "2015-08-07T18:30:00.000Z", 
"2015-08-14T18:30:00.000Z", "2015-08-21T18:30:00.000Z", "2015-08-28T18:30:00.000Z"]

```

**例 2:**

```
<!DOCTYPE html>
<html>

<head>
    <title>
        D3.js | d3.timeSaturday Function
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

        // Calling the timeSaturday function
        // with step value
        var a = d3.timeSaturday.range(start, end, 2);

        // Getting the Saturday dates
        console.log(a);
    </script>
</body>

</html>    
```

**输出:**

```
["2015-07-31T18:30:00.000Z", "2015-08-14T18:30:00.000Z", "2015-08-28T18:30:00.000Z"]

```

**参考:**T2】https://devdocs.io/d3~5/d3-time#timeSaturday