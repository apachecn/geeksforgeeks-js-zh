# D3 . js | D3 . time monkeys()函数

> 原文:[https://www . geeksforgeeks . org/D3-js-D3-timemonas-function/](https://www.geeksforgeeks.org/d3-js-d3-timemondays-function/)

D3.js 中的**D3 . timemonias()函数**用于返回给定起止日期范围内基于星期一的所有日期。

**语法:**

```
d3.timeMondays( start, end, step );
```

**参数:**该函数接受三个参数，如上所述，如下所述:

*   **Start:** This parameter saves the given start date.
*   **End:** This parameter saves the given end date.
*   **Step:** is an optional parameter and a value used to skip the date.

**返回值:**该函数返回基于周一的所有日期。

下面的程序说明了 D3.js 中的**D3 . timemonias()**功能:

**例 1:**

```
<!DOCTYPE html>
<html>

<head>
    <title>
        D3.js | d3.timeMondays() Function
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

        // Calling the timeMondays() function
        // without step value
        var a = d3.timeMondays(start, end);

        // Getting the Monday dates
        console.log(a);
    </script>
</body>

</html>
```

**输出:**

```
["2015-08-02T18:30:00.000Z", "2015-08-09T18:30:00.000Z", 
"2015-08-16T18:30:00.000Z", "2015-08-23T18:30:00.000Z"]

```

**例 2:**

```
<!DOCTYPE html>
<html>

<head>
    <title>
        D3.js | d3.timeMondays() Function
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

        // Calling the timeMondays() function
        // with step value
        var a = d3.timeMondays(start, end, 2);

        // Getting the Monday dates
        console.log(a);
    </script>
</body>

</html>                    
```

**输出:**

```
["2015-08-02T18:30:00.000Z", "2015-08-16T18:30:00.000Z"]

```

**参考:**T2】https://devdocs.io/d3~5/d3-time#timeMondays