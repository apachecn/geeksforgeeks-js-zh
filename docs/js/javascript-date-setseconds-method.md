# JavaScript 日期设置秒()方法

> 原文:[https://www . geesforgeks . org/JavaScript-date-setseconds-method/](https://www.geeksforgeeks.org/javascript-date-setseconds-method/)

下面是**日期设置秒()**方法的例子。

*   **例:**

    ```
    <script>
       // Here a date has been assigned
       // while creating Date object
       var dateobj =
       new Date('October 13, 1996 05:35:32');

       // New second of 52 is being set in above Date
       // Object with the help of setSeconds() method
       dateobj.setSeconds(52);

       // New second from above Date Object is
       // being extracted using getSeconds()
       var B = dateobj.getSeconds();

       // Printing new Second
       document.write(B);
    </script>
    ```

*   **输出:**

    ```
    52
    ```

**date.setSeconds()** 方法用于将秒设置到使用 date()构造函数创建的 Date 对象中。

**语法:**

```
DateObj.setSeconds(seconds_Value)
```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **秒 _ 值:**此参数保存秒的值，用于在 Date()构造函数中设置。

**返回值:**返回由 setSeconds()方法设置的更新秒的新日期。

**注意:****Date obj**是使用 Date()构造函数创建的有效日期对象，我们希望在其中设置第二个。秒的值从 0 到 59。

上述方法的更多代码如下:

**程序 1:** 如果在 Date()构造函数中我们没有给出任何秒，仍然 setSeconds()方法设置新的秒作为它的参数。

```
<script>
   // Here second has not been assigned
   // while creating Date object
   var dateobj = new Date('October 13, 1996');

   // New second of 51 is being set in above Date
   // Object with the help of setSeconds() method
   dateobj.setSeconds(51);

   // New second from above Date Object is
   // being extracted using getSeconds()
   var B = dateobj.getSeconds();

   // Printing new Second
   document.write(B);
</script>
```

**输出:**

```
51
```

**例 2:** 如果 Date()构造函数中没有给定参数，setSeconds()方法仍然设置第二个，但是月、年、日期等变成当前的。这里 42 是新的第二个，3 是当月即 4 月，1 是当前日期，2018 是当前年份。

```
<script>
   // Here nothing has been assigned
   // while creating Date object
   var dateobj = new Date();

   // New second of 42 is being set in above Date
   // Object with the help of setSeconds() method
   dateobj.setSeconds(42);

   // Seconds from above Date Object is
   // being extracted using getSeconds()
   var B = dateobj.getSeconds();

   // Month from above Date Object is
   // being extracted using getMonth()
   var C = dateobj.getMonth();

   // Date from above Date Object is
   // being extracted using getDate()
   var D = dateobj.getDate();

   // Year from above Date Object is
   // being extracted using getFullYear()
   var E = dateobj.getFullYear();

   // Printing new seconds
   document.write(B + "<br />");

   // Printing current month
   document.write(C + "<br />");

   // Printing current date
   document.write(D + "<br />");

   // Printing current year
   document.write(E);
</script>
```

**输出:**

```
42
3
1
2018
```

**例 3:** 如果给定秒 66 的值作为 setSeconds()函数的参数，它将设置 6 为秒，因为秒的范围是从 0 到 59 和(66%60 = 6)。
这里 6 是新的秒，分钟从 35 变成 36，因为秒的范围是从 0 到 59。因此，当 66 作为参数传递给 setSeconds()函数时，它会将相应日期对象中的秒设置为(66%60 = 6)，并将相应日期对象中的分钟数增加(66/60 = 1)。

```
<script>
   // Here date has been assigned
   // while creating Date object
   var dateobj = 
   new Date('October 13, 1996 05:35:32');

   // New second of 66 is being set in above Date
   // Object with the help of setSeconds() function
   dateobj.setSeconds(66);

   // Seconds from above Date Object is
   // being extracted using getSeconds()
   var B = dateobj.getSeconds();

   // Minute from above Date Object is
   // being extracted using getMinutes()
   var C = dateobj.getMinutes();

   // Printing new seconds
   document.write(B + "<br />");

   // Printing minutes
   document.write(C);
</script>
```

**输出:**

```
6
36
```

**支持的浏览器:**JavaScript Date setSeconds()方法支持的浏览器如下:

*   谷歌 Chrome 1 及以上版本
*   边缘 12 及以上
*   Firefox 1 及以上版本
*   Internet Explorer 3 及以上版本
*   歌剧 3 及以上
*   Safari 1 及以上