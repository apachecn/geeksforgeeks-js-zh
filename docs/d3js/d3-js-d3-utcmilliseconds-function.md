# D3 . js | D3 . utcmails()函数

> 原文:[https://www . geesforgeks . org/D3-js-D3-utc 毫秒-function/](https://www.geeksforgeeks.org/d3-js-d3-utcmilliseconds-function/)

D3.js 中的**D3 . utcmails()函数**用于返回在协调世界时(UTC)中给定的开始和结束时间范围内的所有带有日期的毫秒。

**语法:**

```
d3.utcMilliseconds(start, end, step);
```

**参数:**该函数接受三个参数，如下所示:

*   **开始:**这是给定的开始时间。
*   **结束:**这是给定的结束时间。
*   **步骤:**这是用于跳过毫秒的可选值。

**返回值:**该函数返回给定范围内所有可能的毫秒数。

下面的程序说明了 D3.js:
**示例 1:** 中的**D3 . utcmails()**函数

```
<!DOCTYPE html>
<html>

<head>
    <title>
        d3.utcMilliseconds() Function
    </title>
    <script src="https://d3js.org/d3.v4.min.js">
  </script>
</head>

<body>

    <script>
        // Initialising start and end time
        var start = new Date(2015, 07, 01, 4, 20, 10, 1);
        var end = new Date(2015, 07, 01, 4, 20, 10, 5);

        // Calling the utcMilliseconds() function
        // without step value
        var a = d3.utcMilliseconds(start, end);

        // Getting the millisecond values
        console.log(a);
    </script>
</body>

</html>
```

**输出:**

```
["2015-07-31T22:50:10.001Z", "2015-07-31T22:50:10.002Z", 
"2015-07-31T22:50:10.003Z", "2015-07-31T22:50:10.004Z"]

```

**例 2:**

```
<!DOCTYPE html>
<html>

<head>
    <title>
        d3.utcMilliseconds() Function
    </title>
    <script src="https://d3js.org/d3.v4.min.js">
  </script>
</head>

<body>

    <script>
        // Initialising start and end time
        var start = new Date(2015, 07, 01, 4, 20, 10, 1);
        var end = new Date(2015, 07, 01, 4, 20, 10, 5);

        // Calling the utcMilliseconds() function
        // with step value
        var a = d3.utcMilliseconds(start, end, 2);

        // Getting the millisecond values
        console.log(a);
    </script>
</body>

</html>
```

**输出:**

```
["2015-07-31T22:50:10.001Z", "2015-07-31T22:50:10.003Z"]

```

**参考:**T2】https://devdocs.io/d3~5/d3-time#timeMilliseconds