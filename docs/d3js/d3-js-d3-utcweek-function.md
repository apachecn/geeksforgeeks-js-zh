# D3.js | d3.utcWeek 功能

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-utcweek-function/](https://www.geeksforgeeks.org/d3-js-d3-utcweek-function/)

D3.js 中的 **d3.utcWeek 函数**用于返回协调世界时(UTC)中开始和结束日期给定范围内日期和时间的所有周。

**语法:**

```
d3.utcWeek.range(start, end, step);
```

**参数:**该函数接受下面给出的三个参数:

*   **Start:** This parameter saves the given start date.
*   **End:** This parameter saves the given end date.
*   **Step:** is an optional parameter, which holds the value for skipping weeks.

**返回值:**该函数返回给定范围内所有可能的周。

下面的程序说明了 D3.js 中的 **d3.utcWeek** 功能:

**例 1:**

```
<!DOCTYPE html>
<html>
   <head>
      <title>
          D3.js | d3.utcWeek Function
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

         // Calling the utcWeek function
         // without step value
         var a = d3.utcWeek.range(start, end);

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
      <title>
          D3.js | d3.utcWeek Function
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

         // Calling the utcWeek function
         // with step value
         var a = d3.utcWeek.range(start, end, 2);

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

**参考:**T2】https://devdocs.io/d3~5/d3-time#timeWeek