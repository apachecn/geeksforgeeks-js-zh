# D3.js | d3.utcYears()函数

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-utcyears-function/](https://www.geeksforgeeks.org/d3-js-d3-utcyears-function/)

D3.js 中的 **d3.utcYears()函数**用于返回在协调世界时(UTC)中开始日期和结束日期给定范围内的所有年份。

**语法:**

```
d3.utcYears(start, end, step);
```

**参数:**该函数接受下面给出的三个参数:

*   **Start:** This parameter saves the given start date.
*   **End:** This parameter saves the given end date.
*   **Step:** is an optional parameter to save the value for skipping the year.

**返回值:**该函数返回给定范围内所有可能的年份。

下面的程序说明了 D3.js 中的 **d3.utcYears()** 功能:

**例 1:**

```
<!DOCTYPE html>
<html>
   <head>
      <title>
          D3.js | d3.utcYears() Function
      </title>
      <script src =
          "https://d3js.org/d3.v4.min.js">
      </script>
   </head>

   <body>

      <script>

         // Initialising start and end date
         var start = new Date(2015, 01, 01);
         var end = new Date(2020, 01, 01);

         // Calling the utcYears() function
         // without step value
         var a = d3.utcYears(start, end);

         // Getting the years values
         console.log(a);
      </script>
   </body>
</html>
```

**输出:**

```
["2016-01-01T00:00:00.000Z", "2017-01-01T00:00:00.000Z",
 "2018-01-01T00:00:00.000Z", "2019-01-01T00:00:00.000Z",
 "2020-01-01T00:00:00.000Z"]

```

**例 2:**

```
<!DOCTYPE html>
<html>
   <head>
      <title>
          D3.js | d3.utcYears() Function
      </title>
      <script src =
          "https://d3js.org/d3.v4.min.js">
      </script>
   </head>

   <body>

      <script>

         // Initialising start and end date
         var start = new Date(2015, 01, 01);
         var end = new Date(2020, 01, 01);

         // Calling the utcYears() function
         // with step value
         var a = d3.utcYears(start, end, 2);

         // Getting the years values
         console.log(a);
      </script>
   </body>
</html>
```

**输出:**

```
["2016-01-01T00:00:00.000Z", "2018-01-01T00:00:00.000Z",
 "2020-01-01T00:00:00.000Z"]

```

**参考:**T2】https://devdocs.io/d3~5/d3-time#timeYears