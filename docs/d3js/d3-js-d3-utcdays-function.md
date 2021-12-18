# D3.js | d3.utcDays()函数

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-utcdays-function/](https://www.geeksforgeeks.org/d3-js-d3-utcdays-function/)

D3.js 中的 **d3.utcDays()函数**用于返回协调世界时(UTC)中两个给定日期之间的所有日期。

**语法:**

```
d3.utcDays(Start, End, step);
```

**参数:**该函数接受三个参数，如下所示:

*   **开始:**这是给定的开始日期。
*   **结束:**这是给定的结束日期。
*   **步骤:**该参数为可选参数，用于跳过日期。

**返回值:**该函数返回两个给定日期之间的所有日期。

下面的程序说明了 D3.js:
**示例 1:** 中的 **d3.utcDays()** 功能

```
<!DOCTYPE html>
<html>

<head>
    <title>
        D3.js | d3.utcDays() Function
    </title>

    <script src=
        "https://d3js.org/d3.v4.min.js">
    </script>
</head>

<body>
    <script>

        // Initialising start and end date
        var start = new Date(2015, 04, 05);
        var end = new Date(2015, 04, 10);

        // Calling the utcDays() function
        // without step value
        var a = d3.utcDays(start, end);

        // Getting all the in between dates
        console.log(a);
    </script>
</body>

</html>    
```

**输出:**

> 【“2015-05-05T00:00:00.000Z”、“2015-05-06T00:00:00.000Z”、“2015-05-07T00:00:00.000Z”、“2015-05-08T00:00:00.000Z”、“2015-05-09T00:00:00.000Z”】

**例 2:**

```
<!DOCTYPE html>
<html>

<head>
    <title>
        D3.js | d3.utcDays() Function
    </title>

    <script src=
        "https://d3js.org/d3.v4.min.js">
    </script>
</head>

<body>
    <script>

        // Initialising start and end date
        var start = new Date(2015, 04, 05);
        var end = new Date(2015, 04, 10);

        // Calling the utcDays() function
        // with step value
        var a = d3.utcDays(start, end, 2);

        // Getting all the in between dates
        console.log(a);
    </script>
</body>

</html>    
```

**输出:**

```
["2015-05-05T00:00:00.000Z", "2015-05-07T00:00:00.000Z", "2015-05-09T00:00:00.000Z"]

```

**参考:**T2】https://devdocs.io/d3~5/d3-time#timeDays