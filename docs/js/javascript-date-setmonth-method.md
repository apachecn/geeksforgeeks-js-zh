# JavaScript 日期设置月()方法

> 原文:[https://www . geesforgeks . org/JavaScript-date-set month-method/](https://www.geeksforgeeks.org/javascript-date-setmonth-method/)

下面是 **Date setMonth()** 方法的例子。

*   **例:**

    ```
    <script>
       // Here a date has been assigned
       // while creating Date object
       var dateobj = 
       new Date('October 13, 1996 05:35:32');

       // new month of January is being set in above Date
       // Object with the help of setMonth() function
       dateobj.setMonth(0);

       // new month from above Date Object is
       // being extracted using getMonth()
       var B = dateobj.getMonth();

       // Printing new month
       document.write(B);
    </script>
    ```

*   **输出:**

    ```
    0
    ```

**date . setMountain()**方法用于将月份设置为使用 Date()构造函数创建的日期对象。

**语法:**

```
DateObj.setMonth(month_Value);
```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **month_Value:** 此参数保存我们要在使用 date()构造函数创建的日期中设置的月份值。

**返回值:**返回 setMonth()方法设置的新的即更新的月份。

**注意:****Date obj**是使用 Date()构造函数创建的有效日期对象，我们要在其中设置月份。月份的值从 0 到 11，因为一年中从 1 月到 12 月的总月数是 12。值 0 用于 1 月，1 用于 2 月，以此类推，直到 12 月 11 日。

上述方法的更多代码如下:

**程序 1:** 如果在 date()构造函数中我们在创建 date 对象时没有给出任何月份，仍然 setMonth()方法将能够在创建的 Date 对象中设置新的月份。

```
<script>
   // Here month has not been assigned
   // while creating Date object
   var dateobj = new Date('1996, 05:35:32');

   // New month of 2 is being set in above Date
   // Object with the help of setMonth() method
   dateobj.setMonth(2);

   // New month from above Date Object is
   // being extracted using getMonth()
   var B = dateobj.getMonth();

   // Printing new month
   document.write(B);
</script>
```

**输出:**

```
2
```

**程序 2:** 如果 Date()构造函数中没有给定参数，setMonth()方法仍然可以设置月份，但是年、日期等仍然是当前的。这里 11 是 12 月的新月份，1 是当前日期，2018 是当前年份。

```
<script>
   // Here nothing has been assigned
   // while creating Date object
   var dateobj = new Date();

   // New month of 11 is being set in above Date
   // Object with the help of setMonth() method
   dateobj.setMonth(11);

   // Month from above Date Object is
   // being extracted using getMonth()
   var B = dateobj.getMonth();

   // Date from above Date Object is
   // being extracted using getDate()
   var C = dateobj.getDate();

   // Year from above Date Object is
   // being extracted using getFullYear()
   var D = dateobj.getFullYear();

   // Printing new month
   document.write(B + "<br />");

   // Printing current date
   document.write(C + "<br />");

   // Printing current year
   document.write(D);
</script>
```

**输出:**

```
11
1
2018
```

**程序 3:** 如果给定第 15 个月的值作为 setMonth()方法的参数，它将设置 3 为月份，因为月份范围从 0 到 11，因此(15%12 = 3)。
这里 3 是 4 月的新月份，从 1996 年开始年份变成 1997 年，因为月份范围是从 0 到 11，即总计 12，我们将新月份设置为 3，从 1996 年开始年份增加 1 到 1997 年，月份变成 3。

```
<script>
   // Here date has been assigned
   // while creating Date object
   var dateobj = 
   new Date('October 13, 1996 05:35:32');

   // new month of 15 is being set in above Date
   // Object with the help of setMonth() function
   dateobj.setMonth(15);

   // Month from above Date Object is
   // being extracted using getMonth()
   var B = dateobj.getMonth();

   // Year from above Date Object is
   // being extracted using getFullYear()
   var C = dateobj.getFullYear();

   // Printing new month
   document.write(B + "<br />");

   // Printing new year
   document.write(C);
</script>
```

**输出:**

```
3
1997
```

**支持的浏览器:**JavaScript Date setMonth()方法支持的浏览器如下:

*   谷歌 Chrome 1 及以上版本
*   边缘 12 及以上
*   Firefox 1 及以上版本
*   Internet Explorer 3 及以上版本
*   歌剧 3 及以上
*   Safari 1 及以上