# JavaScript 日期设置整年()方法

> 原文:[https://www . geesforgeks . org/JavaScript-date-set full year-method/](https://www.geeksforgeeks.org/javascript-date-setfullyear-method/)

下面是 **Date setFullYear()** 方法的例子。

*   **例:**

    ```
    <script>
       // Here a date has been assigned
       // while creating Date object
       var dateobj =
       new Date('October 13, 1996 05:35:32');

       // New year 1992 is being set in above Date
       // Object with the help of setFullYear() method
       dateobj.setFullYear(1992);

       // New year from above Date Object is
       // being extracted using getFullYear()
       var B = dateobj.getFullYear();

       // Printing new year
       document.write(B);
    </script>
    ```

*   **输出:**

    ```
    1992
    ```

**date.setFullYear()** 方法用于将年份设置到使用 date()构造函数创建的日期对象中。

**语法:**

```
DateObj.setFullYear(year_Value)
```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **year_Value:** 此参数保存日期()构造函数中设置的年份值。

**返回值:**返回用 setFullYear()方法设置的更新年份的新日期。

**注意:****Date obj**是使用 Date()构造函数创建的有效日期对象，我们希望在其中设置年份。

上述方法的更多代码如下:

**程序 1:** 如果在 Date()构造函数中我们没有给出任何年份，那么 setFullYear()方法仍然会设置一个新的年份作为参数。

```
<script>
   // Here year has not been assigned
   // while creating Date object
   var dateobj = 
   new Date('October 13, 05:35:32');

   // new year 1992 is being set in above Date
   // Object with the help of setFullYear() method
   dateobj.setFullYear(1992);

   // New year from above Date Object is
   // being extracted using getFullYear()
   var B = dateobj.getFullYear();

   // Printing new year
   document.write(B);
</script>
```

**输出:**

```
1992
```

**程序 2:** 如果 Date()构造函数中没有给定参数，setFullYear()方法仍然设置年，但是月和日期变成当前的。在输出 2 中，这里是 3 月，因为月份名称从 0 到 11 开始，即 1 月是 0，12 月是 11，30 是当前日期。

```
<script>
   // Here nothing has been assigned
   // while creating Date object
   var dateobj = new Date();

   // new year 2007 is being set in above Date
   // Object with the help of setFullYear() method
   dateobj.setFullYear(2007);

   // Year from above Date Object is
   // being extracted using getFullYear()
   var B = dateobj.getFullYear();

   // Month from above Date Object is
   // being extracted using getMonth()
   var C = dateobj.getMonth();

   // Date from above Date Object is
   // being extracted using getDate()
   var D = dateobj.getDate();

   // Printing new year
   document.write(B + "<"<br />">");

   // Printing current month
   document.write(C + "<"<br />">");

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

**支持的浏览器:**JavaScript Date set full year()方法支持的浏览器如下:

*   谷歌 Chrome 1 及以上版本
*   边缘 12 及以上
*   Firefox 1 及以上版本
*   Internet Explorer 4 及以上版本
*   歌剧 4 及以上
*   Safari 1 及以上