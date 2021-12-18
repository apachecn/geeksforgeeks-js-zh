# D3.js | d3.utcTuesdays()功能

> 原文:[https://www . geesforgeks . org/D3-js-D3-utc Tuesdays-function/](https://www.geeksforgeeks.org/d3-js-d3-utctuesdays-function/)

D3.js 中的 **d3.utcTuesdays()函数**用于返回以协调世界时(UTC)中给定的开始和结束日期范围内基于星期二的所有日期。

**语法:**

```
d3.utcTuesdays(start, end, step);
```

**参数:**该函数接受三个参数，如下所示:

*   **开始:**这是给定的开始日期。
*   **结束:**这是给定的结束日期。
*   **步骤:**这是用于跳过日期的可选值。

**返回值:**该函数返回基于星期二的所有日期。

下面的程序说明了 D3.js 中的 **d3.utcTuesdays()** 功能:
T3】示例 1:

```
<!DOCTYPE html>
<html>

<head>
    <title>
        D3.js | d3.utcTuesdays() Function
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

        // Calling the utcTuesdays() function
        // without step value
        var a = d3.utcTuesdays(start, end);

        // Getting the Tuesday dates
        console.log(a);
    </script>
</body>

</html>    
```

**输出:**

> 【“2015-08-04T00:00:00.000Z”、“2015-08-11T00:00:00.000Z”、“2015-08-18T00:00:00.000Z”、“2015-08-25T00:00:00.000Z”】

**例 2:**

```
<!DOCTYPE html>
<html>

<head>
    <title>
        D3.js | d3.utcTuesdays() Function
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

        // Calling the utcTuesdays() function
        // with step value
        var a = d3.utcTuesdays(start, end, 2);

        // Getting the Tuesday dates
        console.log(a);
    </script>
</body>

</html>    
```

**输出:**

```
["2015-08-04T00:00:00.000Z", "2015-08-18T00:00:00.000Z"]

```