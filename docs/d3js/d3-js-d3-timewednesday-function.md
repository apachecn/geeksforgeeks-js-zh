# D3 . js | D3 . time 星期三()功能

> 原文:[https://www . geesforgeks . org/D3-js-D3-time 星期三-function/](https://www.geeksforgeeks.org/d3-js-d3-timewednesday-function/)

D3.js 中的**D3 . time 星期三功能**用于返回给定起止日期范围内所有基于星期三的日期。

**语法:**

```
d3.timeWednesday.range(start, end, step);
```

**参数:**该函数接受下面给出的三个参数:

*   **Start:** This parameter saves the given start date.
*   **End:** This parameter saves the given end date.
*   **Step:** This is an optional value for skipping the date.

**返回值:**该函数返回基于周三的所有日期。

下面的程序说明了 D3.js 中的**D3 . time 星期三**功能:

**例 1:**

```
<!DOCTYPE html>
<html>
      <head>
      <title>
          D3.js | d3.timeWednesday() Function 
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

         // Calling the timeWednesday function
         // without step value
         var a = d3.timeWednesday.range(start, end);

         // Getting the Wednesday dates
         console.log(a);
      </script>
   </body>
</html>
```

**输出:**

```
["2015-08-04T18:30:00.000Z", "2015-08-11T18:30:00.000Z",
 "2015-08-18T18:30:00.000Z", "2015-08-25T18:30:00.000Z"]

```

**例 2:**

```
<!DOCTYPE html>
<html>
   <head>
      <title>
          D3.js | d3.timeWednesday() Function 
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

         // Calling the timeWednesday function
         // with step value
         var a = d3.timeWednesday.range(start, end, 2);

         // Getting the Wednesday dates
         console.log(a);
      </script>
   </body>
</html>
```

**输出:**

```
["2015-08-04T18:30:00.000Z", "2015-08-18T18:30:00.000Z"]

```

**参考:**T2】https://devdocs.io/d3~5/d3-time#timeWednesday