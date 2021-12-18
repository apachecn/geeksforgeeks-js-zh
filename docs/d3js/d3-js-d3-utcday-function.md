# D3.js | d3.utcDay()功能

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-utcday-function/](https://www.geeksforgeeks.org/d3-js-d3-utcday-function/)

D3.js 中的**D3 . utchday()函数**用于以协调世界时(UTC)的**“YYYY-MM-DD”**格式返回日期。

**语法:**

```
d3.utcDay(Date);
```

**参数:**该功能接受一个参数**【日期】**。

**返回值:**该函数以特定的格式返回给定的日期。

以下程序说明了 D3.js:
**示例 1:** 中的 **d3.utcDay()** 功能

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

        // calling d3.utcDay()
        var day = d3.utcDay(now);

        // Getting the date
        console.log(day);
    </script>
</body>

</html>
```

**输出:**

```
"2019-07-20T00:00:00.000Z"

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

        // Calling the utcDay() function to
        // calculate the difference between two dates
        var a = d3.utcDay.count(start, end);

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