# D3.js | d3.utcWednesdays()功能

> 原文:[https://www . geesforgeks . org/D3-js-D3-utc Wednesdays-function/](https://www.geeksforgeeks.org/d3-js-d3-utcwednesdays-function/)

D3.js 中的 **d3.utcWednesdays()函数**用于返回以协调世界时(UTC)中给定的开始和结束日期范围内基于星期三的所有日期。

**语法:**

```
d3.utcWednesdays(start, end, step);
```

**参数:**该函数接受下面给出的三个参数:

*   **Start:** This parameter saves the given start date.
*   **End:** This parameter saves the given end date.
*   **Step:** This is an optional value for skipping the date.

**返回值:**此函数返回以协调世界时(UTC)中的星期三为基础的所有日期。

下面的程序说明了 D3.js 中的 **d3.utcWednesdays()** 功能:

**例 1:**

```
<!DOCTYPE html>
<html>
   <head>
      <title>
          D3.js | d3.utcWednesdays() Function
      </title>
      <script src =
          "https://d3js.org/d3.v4.min.js">
      </script>
   </head>

   <body>

      <script>

         // Initialising start and end date
         var start = new Date(2015, 07, 01);
         var end = new Date(2015, 07, 30);

         // Calling the utcWednesdays() function
         // without step value
         var a = d3.utcWednesdays(start, end);

         // Getting the Wednesday dates
         console.log(a);
      </script>
   </body>
</html>
```

**输出:**

```
["2015-08-05T00:00:00.000Z","2015-08-12T00:00:00.000Z",
 "2015-08-19T00:00:00.000Z","2015-08-26T00:00:00.000Z"]

```

**例 2:**

```
<!DOCTYPE html>
<html>
   <head>
      <title>
          D3.js | d3.utcWednesdays() Function
      </title>
      <script src =
          "https://d3js.org/d3.v4.min.js">
      </script>
   </head>

   <body>

      <script>

         // Initialising start and end date
         var start = new Date(2015, 07, 01);
         var end = new Date(2015, 07, 30);

         // Calling the utcWednesdays() function
         // with step value
         var a = d3.utcWednesdays(start, end, 2);

         // Getting the Wednesday dates
         console.log(a);
      </script>
   </body>
</html>
```

**输出:**

```
["2015-08-05T00:00:00.000Z","2015-08-19T00:00:00.000Z"]

```

**参考:**T2】https://devdocs.io/d3~5/d3-time#timeWednesdays