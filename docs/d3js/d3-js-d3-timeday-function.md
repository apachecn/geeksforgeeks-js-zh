# D3.js | d3.timeDay()函数

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-timeday-function/](https://www.geeksforgeeks.org/d3-js-d3-timeday-function/)

D3.js 中的 **d3.timeDay()函数**用于返回**格式的【YYYY-MM-DD】**日期。

**语法:**

```
d3.timeDay(Date);
```

**参数:**该功能接受一个参数**【日期】**。

**返回值:**该函数以特定的格式返回给定的日期。

下面的程序说明了 D3.js 中的 **d3.timeDay()** 函数:
T3】示例 1:

```
<!DOCTYPE html>
<html>

<head>
    <script src=
        "https://d3js.org/d3.v4.min.js">
  </script>
</head>

<body>

    <script>
        // Initialising a current date
        var now = new Date;

        // calling d3.timeDay()
        var day = d3.timeDay(now);

        // Getting the date
        console.log(day);
    </script>
</body>

</html>
```

**输出:**

```
"2019-07-19T18:30:00.000Z"

```

**示例 2:** 下面的代码计算两个给定日期之间的差异。

```
<!DOCTYPE html>
<html>

<head>
    <script src=
            "https://d3js.org/d3.v4.min.js">
  </script>
</head>

<body>

    <script>
        // Initialising start and end date
        var start = new Date(2015, 02, 01);
        var end = new Date(2015, 02, 04);

        // Calling the timeDay() function to
        // calculate the difference between two dates
        var a = d3.timeDay.count(start, end);

        // Getting the calculated dates
        console.log(a);
    </script>
</body>

</html>
```

**输出:**

```
3

```