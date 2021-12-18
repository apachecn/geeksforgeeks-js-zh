# D3.js | d3.utcHours()功能

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-utchours-function/](https://www.geeksforgeeks.org/d3-js-d3-utchours-function/)

D3.js 中的 **d3.utcHours()函数**用于返回在协调世界时(UTC)中给定的开始和结束时间范围内所有带有日期的小时。

**语法:**

```
d3.utcHours(start, end, step);
```

**参数:**该函数接受下面给出的三个参数:

*   **Start:** This parameter stores the given start time.
*   **End:** This parameter saves the given end time.
*   **Step:** This is an optional value for skipping hours.

**返回值:**该函数返回给定范围内所有可能的小时数。

下面的程序说明了 D3.js 中的 **d3.utcHours()** 功能:

**例 1:**

```
<!DOCTYPE html>
<html>
   <head>
      <title>
          D3.js | d3.utcHours() Function 
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

         // Calling the utcHours() function
         // without step value
         var a = d3.utcHours(start, end);

         // Getting the hours values
         console.log(a);
      </script>
   </body>
</html>
```

**输出:**

```
["2015-07-31T23:00:00.000Z", "2015-08-01T00:00:00.000Z",
 "2015-08-01T01:00:00.000Z", "2015-08-01T02:00:00.000Z"]

```

**例 2:**

```
<!DOCTYPE html>
<html>
   <head>
      <title>
          D3.js | d3.utcHours() Function 
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

         // Calling the utcHours() function
         // with step value
         var a = d3.utcHours(start, end, 2);

         // Getting the hour values
         console.log(a);
      </script>
   </body>
</html>
```

**输出:**

```
["2015-07-31T20:00:00.000Z", "2015-07-31T22:00:00.000Z", 
 "2015-08-01T00:00:00.000Z"]

```

**参考:**T2】https://devdocs.io/d3~5/d3-time#timeHours