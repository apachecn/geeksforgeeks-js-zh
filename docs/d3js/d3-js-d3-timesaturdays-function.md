# D3 . js | D3 . timestaturdays()函数

> 原文:[https://www . geesforgeks . org/D3-js-D3-timestaurdays-function/](https://www.geeksforgeeks.org/d3-js-d3-timesaturdays-function/)

D3.js 中的**D3 . timestaturdays()函数**用于返回给定起止日期范围内基于周六的所有日期。

**语法:**

```
d3.timeSaturdays(start, end, step);
```

**参数:**该函数接受三个参数，如下所示:

*   **开始:**这是给定的开始日期。
*   **结束:**这是给定的结束日期。
*   **步骤:**这是用于跳过日期的可选值。

**返回值:**该函数返回基于周六的所有日期。

下面的程序说明了 D3.js 中的**D3 . timestaurdays()**函数:
T3】例 1:

```
<!DOCTYPE html>
<html>

<head>
    <title>
        D3.js | d3.timeSaturdays() Function
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

        // Calling the timeSaturdays() function
        // without step value
        var a = d3.timeSaturdays(start, end);

        // Getting the Saturday dates
        console.log(a);
    </script>
</body>

</html>
```

**输出:**

> 【“2015-07-31t 18:30:00.000 z”“2015-08-07t 18:30:00.000 z”“2015-08-14t 18:30:00.000 z”“2015-08-21t 18:30:00.000 z”“2015-08-28t 18:30:00.000 z”】

**例 2:**

```
<!DOCTYPE html>
<html>

<head>
    <title>
        D3.js | d3.timeSaturdays() Function
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

        // Calling the timeSaturdays() function
        // with step value
        var a = d3.timeSaturdays(start, end, 2);

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

**参考:**T2】https://devdocs.io/d3~5/d3-time#timeSaturdays