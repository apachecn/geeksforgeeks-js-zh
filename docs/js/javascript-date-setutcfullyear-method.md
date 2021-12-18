# JavaScript Date setutc full year()方法

> 原文:[https://www . geeksforgeeks . org/JavaScript-date-setutc full year-method/](https://www.geeksforgeeks.org/javascript-date-setutcfullyear-method/)

下面是 Date setUTCFullYear()方法的示例。

*   **例:**

    ```
    <script>
       // Here a date has been assigned according
       // to universal time while creating Date object
       var dateobj = 
       new Date('October 13, 1996 05:35:32 GMT-3:00');

       // New year 1992 is being set in above Date
       // Object with the help of setUTCFullYear() method
       dateobj.setUTCFullYear(1992);

       // New year from above Date Object is
       // being extracted using getUTCFullYear()
       var B = dateobj.getUTCFullYear();

       // Printing new year
       document.write(B);
    </script>
    ```

*   **输出:**

    ```
    1992
    ```

**date.setUTCFullYear()** 方法用于根据使用 date()构造函数创建的世界时将年设置为日期对象。

**语法:**

```
DateObj.setUTCFullYear(year_Value);
```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **year_Value:** 此参数保存年的值，用于在 date()构造函数中设置。

**返回值:**根据 setUTCFullYear()方法设置的世界时返回新的即更新的年份。

**注意:****Date obj**是使用 Date()构造函数创建的有效日期对象，我们希望在其中设置年份。

上述方法的更多代码如下:
**程序 1:** 如果在 Date()构造函数中我们没有给出任何年份，仍然 setUTCFullYear()方法将能够根据作为其参数给出的世界时来设置新的一年。

```
<script>
   // Here year according to universal time has not
   // been assigned while creating Date object
   var dateobj = 
   new Date('October 13, 05:35:32 GMT-3:00');

   // New year 1992 is being set in above Date
   // Object with the help of setUTCFullYear() method
   dateobj.setUTCFullYear(1992);

   // New year from above Date Object is
   // being extracted using getUTCFullYear()
   var B = dateobj.getUTCFullYear();

   // Printing new year
   document.write(B);
</script>
```

**输出:**

```
1992
```

**程序 2:** 如果在 Date()构造函数中没有给定任何参数，setUTCFullYear()方法仍然能够在创建的 Date 对象中设置一年，但是月和日期仍然是当前的。
在输出 2 中，这里是 3 月，因为月份名称从 0 到 11 开始，即 0 代表 1 月，11 代表 12 月，30 是当前日期。

```
<script>
   // Here nothing has been assigned
   // while creating Date object
   var dateobj = new Date();

   // New year 2007 is being set in above Date
   // Object with the help of setUTCFullYear() method
   dateobj.setUTCFullYear(2007);

   // Year from above Date Object is
   // being extracted using getUTCFullYear()
   var B = dateobj.getUTCFullYear();

  // Month from above Date Object is
  // being extracted using getUTCMonth()
  var C = dateobj.getUTCMonth();

  // Date from above Date Object is
  // being extracted using getUTCDate()
  var D = dateobj.getUTCDate();

  // Printing new year
  document.write(B + "<br />");

  // Printing current month
  document.write(C + "<br />");

  // Printing current date
  document.write(D);
</script>
```

**输出:**

```
2007
2
30
```

**支持的浏览器:**支持的浏览器**JavaScript Date setutchfully year()方法**如下:

*   谷歌 Chrome 1 及以上版本
*   边缘 12 及以上
*   Firefox 1 及以上版本
*   Internet Explorer 4 及以上版本
*   歌剧 4 及以上
*   Safari 1 及以上