# D3.js | d3.utcWeeks()函数

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-utcweeks-function/](https://www.geeksforgeeks.org/d3-js-d3-utcweeks-function/)

D3.js 中的 **d3.utcWeeks()函数**用于返回协调世界时(UTC)中开始和结束日期给定范围内日期和时间的所有周。

**语法:**

```
d3.utcWeeks(start, end, step);
```

**参数:**该函数接受三个参数，如下所示:

*   **开始:**这是给定的开始日期。
*   **结束:**这是给定的结束日期。
*   **步骤:**这是用于跳过周的可选值。

**返回值:**该函数返回给定范围内所有可能的周。

以下程序说明了 D3.js:
**示例 1:** 中的 **d3.utcWeeks()** 功能

```
<!DOCTYPE html>
<html>

<head>
    <title>
        d3.utcWeeks() Function
    </title>
    <script src=
            "https://d3js.org/d3.v4.min.js">
    </script>
</head>

<body>

    <script>
        // Initialising start and end date
        var start = new Date(2015, 01, 01);
        var end = new Date(2015, 02, 01);

        // Calling the utcWeeks() function
        // without step value
        var a = d3.utcWeeks(start, end);

        // Getting the week values
        console.log(a);
    </script>
</body>

</html>
```

**输出:**

```
["2015-02-01T00:00:00.000Z", "2015-02-08T00:00:00.000Z", 
"2015-02-15T00:00:00.000Z", "2015-02-22T00:00:00.000Z"]

```

**例 2:**

```
<!DOCTYPE html>
<html>

<head>
    <script src=
            "https://d3js.org/d3.v4.min.js">
    </script>
    <title>
        d3.utcWeeks() Function
    </title>
</head>

<body>

    <script>
        // Initialising start and end date
        var start = new Date(2015, 01, 01);
        var end = new Date(2015, 02, 01);

        // Calling the utcWeeks() function
        // with step value
        var a = d3.utcWeeks(start, end, 2);

        // Getting the week values
        console.log(a);
    </script>
</body>

</html>
```

**输出:**

```
["2015-02-01T00:00:00.000Z", "2015-02-15T00:00:00.000Z"]

```

**参考:**T2】https://devdocs.io/d3~5/d3-time#timeWeeks