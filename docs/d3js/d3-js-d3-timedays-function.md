# D3.js | d3.timeDays()函数

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-timedays-function/](https://www.geeksforgeeks.org/d3-js-d3-timedays-function/)

D3.js 中的 **d3.timeDays()函数**用于*返回两个给定日期*之间的所有日期。

**语法:**

```
d3.timeDays(Start, End, step);
```

**参数:**该功能接受以下给出的三个参数:

*   **Start:** This is the given start date.
*   **End:** This is the given end date.
*   **Step:** This parameter is optional and is used to skip the date.

**返回值:**该函数返回两个给定日期之间的所有日期。

下面的程序说明了 D3.js 中的 **d3.timeDays()** 功能:

**例 1:**

```
<!DOCTYPE html>
<html>

<head>
    <script src="https://d3js.org/d3.v4.min.js">
  </script>
</head>

<body>

    <script>
        // Initialising start and end date
        var start = new Date(2015, 04, 05);
        var end = new Date(2015, 04, 10);

        // Calling the timeDays() function
        // without step value
        var a = d3.timeDays(start, end);

        // Getting all the in between dates
        console.log(a);
    </script>
</body>

</html>
```

**输出:**

> 【“2015-05-04 t18:30:00.000 z”“2015-05-05 t18:30:00.000 z”“2015-05-06 t18:30:00.000 z”“2015-05-07 t18:30:00.000 z”“2015-05-08 t18:30:00

**例 2:**

```
<!DOCTYPE html>
<html>

<head>
    <script src="https://d3js.org/d3.v4.min.js">
  </script>
</head>

<body>

    <script>
        // Initialising start and end date
        var start = new Date(2015, 04, 05);
        var end = new Date(2015, 04, 08);

        // Calling the timeDays() function
        // with step value
        var a = d3.timeDays(start, end, 2);

        // Getting all the in between dates
        console.log(a);
    </script>
</body>

</html>
```

**输出:**

```
["2015-05-04T18:30:00.000Z","2015-05-06T18:30:00.000Z"]

```

**参考:**T2】https://devdocs.io/d3~5/d3-time#timeDays