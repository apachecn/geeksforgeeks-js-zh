# D3.js | d3.timeWeeks()功能

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-timeweeks-function/](https://www.geeksforgeeks.org/d3-js-d3-timeweeks-function/)

D3.js 中的 **d3.timeWeeks()函数**用于返回日期和时间在给定的开始和结束日期范围内的所有周。

**语法:**

```
d3.timeWeeks( start, end, step );
```

**参数:**该函数接受下面给出的三个参数:

*   **Start:** This parameter saves the given start date.
*   **End:** This parameter saves the given end date.
*   **Step:** is an optional parameter to save the value for skipping weeks.

**返回值:**该函数返回给定范围内所有可能的周。

下面的程序说明了 D3.js 中的 **d3.timeWeeks()** 功能:

**例 1:**

```
<!DOCTYPE html>
<html>

<head>
    <title>
        D3.js | d3.timeWeeks() Function
    </title>

    <script src = 
        "https://d3js.org/d3.v4.min.js">
    </script>
</head>

<body>
    <script>

        // Initialising start and end date
        var start = new Date(2015, 01, 01);
        var end = new Date(2015, 02, 01);

        // Calling the timeWeeks() function
        // without step value
        var a = d3.timeWeeks(start, end);

        // Getting the week values
        console.log(a);
    </script>

</html>    
```

**输出:**

```
["2015-01-31T18:30:00.000Z", "2015-02-07T18:30:00.000Z", 
"2015-02-14T18:30:00.000Z", "2015-02-21T18:30:00.000Z"]

```

**例 2:**

```
<!DOCTYPE html>
<html>

<head>
    <title>
        D3.js | d3.timeWeeks() Function
    </title>

    <script src = 
        "https://d3js.org/d3.v4.min.js">
    </script>
</head>

<body>
    <script>

        // Initialising start and end date
        var start = new Date(2015, 01, 01);
        var end = new Date(2015, 02, 01);

        // Calling the timeWeeks() function
        // with step value
        var a = d3.timeWeeks(start, end, 2);

        // Getting the week values
        console.log(a);
    </script>

</html>    
```

**输出:**

```
["2015-01-31T18:30:00.000Z", "2015-02-14T18:30:00.000Z"]

```

**参考:**T2】https://devdocs.io/d3~5/d3-time#timeWeeks