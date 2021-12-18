# JavaScript 日期设置日期()方法

> 原文:[https://www . geesforgeks . org/JavaScript-date-setutchdate-method/](https://www.geeksforgeeks.org/javascript-date-setutcdate-method/)

下面是**Date setutctdate()**方法的例子。

*   **例:**

    ```
    <script>
       // Here a date has been assigned according 
       // to universal time while creating Date object
       var dateobj = 
       new Date('October 13, 1996 05:35:32 GMT-3:00');

       // New date 15 of the month is being set in above 
       // Date Object with the help of setDate() method
       dateobj.setUTCDate(15);

       // New date of the month according to universal 
       // time from above Date Object is being extracted 
       // using getDate()
       var B = dateobj.getUTCDate();

       // Printing new date of the month
       document.write(B);
    </script>
    ```

*   **输出:**

    ```
    15
    ```

**date . setutctdate()**方法用于将一个月中根据世界时的日期设置到一个日期对象中，该日期对象是使用 Date()构造函数创建的。

**语法:**

```
DateObj.setUTCDate(date_Value);
```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **日期 _ 值**该参数保存我们想要在使用 date()构造函数创建的日期对象中设置的日期值。

**返回值:**返回由 setUTCDate()方法设置的当月新日期，即更新日期。月份日期是一个从 1 到 31 的整数值。

上述方法的更多代码如下:

**程序 1:** 这里我们知道月份的日期在 1 到 31 之间，但是如果我们试图将日期设置为 33，它会将下个月的日期设置为 2，因为 33-31=2，并且这个日期 2 成为上个月的下一个日期。

在上面的输出中，2 是 11 月的日期，10 是 11 月，因为月份名称从 0 到 11 开始，即 1 月为 0，12 月为 11。

```
<script>
   // Here a date according to universal time has
   // been assigned while creating Date object
   var dateobj = 
   new Date('October 13, 1996 05:35:32 GMT-3:00');

   // New date 33 of the month is being set in above 
   // Date Object with the help of setUTCDate() function
   dateobj.setUTCDate(33);

   // New date of the month from above Date Object is
   // being extracted using getUTCDate()
   var B = dateobj.getUTCDate();

   // New month from above Date Object is
   // being extracted using getUTCMonth()
   var C = dateobj.getUTCMonth();

   // Printing new date of the month
   document.write(B + "<br />");

   // Printing new month
   document.write(C);
</script>
```

**输出:**

```
2
10
```

**程序 2:** 如果在 date()构造函数中，我们在创建 date 对象时没有给出一个月中的任何日期，那么 setUTCDate()方法仍然能够在创建的 Date 对象中设置作为其参数给出的新日期。

```
<script>
   // Here date according to universal time has
   // not been assigned while creating Date object
   var dateobj = 
   new Date('October, 1996 05:35:32 GMT-3:00');

   // New date 12 of the month is being set in above Date
   // Object with the help of setUTCDate() method
   dateobj.setUTCDate(12);

   // New date of the month from above Date Object is
   // being extracted using getUTCDate()
   var B = dateobj.getUTCDate();

   // Printing new date of the month
   document.write(B);
</script>
```

**输出:**

```
12
```

**程序 3:** 如果 Date()构造函数中没有给定参数，setDate()函数仍然可以设置日期，但是月份仍然是当前的。

```
<script>
   // Here nothing has been assigned
   // while creating Date object
   var dateobj = new Date();

   // new date 13 of the month is being set in above
   // Date Object with the help of setUTCDate() method
   dateobj.setUTCDate(13);

   // Date of the month from above Date Object is
   // being extracted using getUTCDate()
   var B = dateobj.getUTCDate();

   // Month from above Date Object is
   // being extracted using getUTCMonth()
   var C = dateobj.getUTCMonth();

   // Printing new date of the month
   document.write(B + "<br />");

   // Printing new month
   document.write(C);
</script>
```

**输出:**

```
13
3
```

**程序 4:** 如果当月新日期设置为零(0)，新日期将设置为上月最后一天。

```
<script>
   // Here a date according to universal time
   // has been assigned while creating Date object
   var dateobj = 
   new Date('October 13, 1996 05:35:32 GMT-3:00');

   // New date 0 of the month is being set in above 
   // Date Object with the help of setUTCDate() method
   dateobj.setUTCDate(0);

   // Date of the month from above Date Object is
   // being extracted using getUTCDate()
   var B = dateobj.getUTCDate();

   // Month from above Date Object is
   // being extracted using getUTCMonth()
   var C = dateobj.getUTCMonth();

   // Printing new date of the month
   document.write(B + "<br>");

   // Printing new month
   document.write(C);
</script>
```

**输出:**

```
30
8
```

**支持的浏览器:**JavaScript Date setutctdate()方法支持的浏览器如下:

*   谷歌 Chrome 1 及以上版本
*   边缘 12 及以上
*   Firefox 1 及以上版本
*   Internet Explorer 4 及以上版本
*   歌剧 4 及以上
*   Safari 1 及以上