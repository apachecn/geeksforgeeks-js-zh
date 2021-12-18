# D3.js | d3.timeHours()功能

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-timehours-function/](https://www.geeksforgeeks.org/d3-js-d3-timehours-function/)

D3.js 中的 **d3.timeHours()功能**用于返回给定开始和结束时间范围内所有带有日期的小时。

**语法:**

```
d3.timeHours(start, end, step);
```

**参数:**该函数接受下面给出的三个参数:

*   **Start:** This parameter stores the given start time.
*   **End:** This parameter saves the given end time.
*   **Step:** This is an optional value for skipping hours.

**返回值:**该函数返回给定范围内所有可能的小时数。

以下程序说明了 D3.js 中的 **d3.timeHours()** 功能:

**例 1:**

```
<!DOCTYPE html>
<html>
   <head>
      <title>
          D3.js | d3.timeHours() Function 
      </title>
      <script src =
          "https://d3js.org/d3.v4.min.js">
      </script>
   </head>

   <body>

      <script>

         // Initialising start and end time
         var start = new Date(2015, 07, 01, 4, 20);
         var end = new Date(2015, 07, 01, 8, 20);

         // Calling the timeHours() function
         // without step value
         var a = d3.timeHours(start, end);

         // Getting the hours values
         console.log(a);
      </script>
   </body>
</html>
```

**输出:**

```
["2015-07-31T23:30:00.000Z", "2015-08-01T00:30:00.000Z", 
 "2015-08-01T01:30:00.000Z", "2015-08-01T02:30:00.000Z"]

```

**例 2:**

```
<!DOCTYPE html>
<html>
   <head>
      <title>
          D3.js | d3.timeHours() Function 
      </title>
      <script src =
          "https://d3js.org/d3.v4.min.js">
      </script>
   </head>

   <body>

      <script>

         // Initialising start and end time
         var start = new Date(2015, 07, 01, 1, 20);
         var end = new Date(2015, 07, 01, 6, 20);

         // Calling the timeHours() function
         // with step value
         var a = d3.timeHours(start, end, 2);

         // Getting the hour values
         console.log(a);
      </script>
   </body>
</html>
```

**输出:**

```
["2015-07-31T20:30:00.000Z", "2015-07-31T22:30:00.000Z", 
 "2015-08-01T00:30:00.000Z"]

```

**参考:**T2】https://devdocs.io/d3~5/d3-time#timeHours