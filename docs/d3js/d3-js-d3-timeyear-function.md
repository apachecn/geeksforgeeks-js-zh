# D3.js | d3.timeYear 函数

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-timeyear-function/](https://www.geeksforgeeks.org/d3-js-d3-timeyear-function/)

D3.js 中的 **d3.timeYear 函数**用于返回日期在给定起止日期范围内的所有年份。

**语法:**

```
d3.timeYear.range(start, end, step);
```

**参数:**该函数接受下面给出的三个参数:

*   **Start:** This parameter saves the given start date.
*   **End:** This parameter saves the given end date.
*   **Step:** is an optional parameter to save the value for skipping the year.

**返回值:**该函数返回给定范围内所有可能的年份。

以下程序说明了 D3.js 中的 **d3.timeYear** 功能:

**例 1:**

```
<!DOCTYPE html>
<html>
   <head>
      <title>
          D3.js | d3.timeYear Function
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

         // Calling the timeYear function
         // without step value
         var a = d3.timeYear.range(start, end);

         // Getting the years values
         console.log(a);
      </script>
   </body>
</html>
```

**输出:**

```
["2015-12-31T18:30:00.000Z","2016-12-31T18:30:00.000Z",
 "2017-12-31T18:30:00.000Z","2018-12-31T18:30:00.000Z",
 "2019-12-31T18:30:00.000Z"]

```

**例 2:**

```
<!DOCTYPE html>
<html>
   <head>
      <title>
          D3.js | d3.timeYear Function
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

         // Calling the timeYear function
         // with step value
         var a = d3.timeYear.range(start, end, 2);

         // Getting the years values
         console.log(a);
      </script>
   </body>
</html>
```

**输出:**

```
["2015-12-31T18:30:00.000Z","2017-12-31T18:30:00.000Z",
 "2019-12-31T18:30:00.000Z"]

```

**参考:**T2】https://devdocs.io/d3~5/d3-time#timeYear