# D3.js | d3.timeMonth 功能

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-timemonth-function/](https://www.geeksforgeeks.org/d3-js-d3-timemonth-function/)

D3.js 中的 **d3.timeMonth 函数**用于返回日期在给定起止日期范围内的所有月份。

**语法:**

```
d3.timeMonth.range(start, end, step);
```

**参数:**该函数接受下面给出的三个参数:

*   **Start:** This parameter saves the given start date.
*   **End:** This parameter saves the given end date.
*   **Step:** is an optional parameter, which holds the value for skipping the month.

**返回值:**该函数返回给定范围内所有可能的月份。

下面的程序说明了 D3.js 中的 **d3.timeMonth** 功能:

**例 1:**

```
<!DOCTYPE html>
<html>
   <head>
      <title>
          D3.js | d3.timeMonth Function
      </title>
      <script src =
          "https://d3js.org/d3.v4.min.js">
      </script>
   </head>

   <body>

      <script>

         // Initialising start and end date
         var start = new Date(2015, 01, 01);
         var end = new Date(2015, 05, 01);

         // Calling the timeMonth function
         // without step value
         var a = d3.timeMonth.range(start, end);

         // Getting the months values
         console.log(a);
      </script>
   </body>
</html>
```

**输出:**

```
["2015-01-31T18:30:00.000Z", "2015-02-28T18:30:00.000Z", 
"2015-03-31T18:30:00.000Z", "2015-04-30T18:30:00.000Z"]

```

**例 2:**

```
<!DOCTYPE html>
<html>
   <head>
      <script src = 
          "https://d3js.org/d3.v4.min.js">
      </script>

      <title>
          D3.js | d3.timeMonth Function
      </title>
   </head>

   <body>

      <script>

         // Initialising start and end date
         var start = new Date(2015, 01, 01);
         var end = new Date(2015, 05, 01);

         // Calling the timeMonth function
         // with step value
         var a = d3.timeMonth.range(start, end, 2);

         // Getting the months values
         console.log(a);
      </script>
   </body>
</html>
```

**输出:**

```
["2015-01-31T18:30:00.000Z", "2015-03-31T18:30:00.000Z"]

```

**参考:**T2】https://devdocs.io/d3~5/d3-time#timeMonth