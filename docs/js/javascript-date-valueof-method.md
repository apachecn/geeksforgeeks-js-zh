# JavaScript 日期值 Of()方法

> 原文:[https://www . geesforgeks . org/JavaScript-date-value of-method/](https://www.geeksforgeeks.org/javascript-date-valueof-method/)

下面是**日期值()**方法的例子。

*   **例:**

    ```
    <script>
       // Here a date has been assigned
       // while creating Date object
       var dateobj = 
       new Date('October 15, 1996 05:35:32');

       // Getting the number of milliseconds between 
       // 1 January 1970 00:00:00
       // UTC and the given date as the content of 
       // the above Date() constructor.
       var B = dateobj.valueOf();

       // Printing the calculated number
       // of milliseconds.
       document.write(B);
    </script>
    ```

*   **输出:**

    ```
    845337932000
    ```

**date.valueOf()** 方法用于获取世界协调时 1970 年 1 月 1 日 00:00:00 到给定日期之间的毫秒数。
**语法:**

```
dateObj.valueOf()
```

**参数:**此方法不接受任何参数。它只是与使用 Date()构造函数创建的 Date 对象一起使用。

**返回值:**返回 1970 年 1 月 1 日 00:00:00 UTC 到给定日期之间的毫秒数，作为 date()构造函数的内容。

**注意:****DateObj**是使用 Date()构造函数创建的有效日期对象，其内容用于获取世界协调时 1970 年 1 月 1 日 00:00:00 和给定日期之间的毫秒数作为 Date()构造函数的内容。

上述方法的更多代码如下:

**程序 1:** 如果在创建日期对象时没有作为参数传递任何内容，但仍然是 valueOf()方法返回 1970 年 1 月 1 日 00:00:00 UTC 和当前日期之间的毫秒数。

```
<script>
   // Here nothing has been assigned
   // while creating Date object
   var dateobj = new Date();

   // Getting the number of milliseconds between 
   // 1 January 1970 00:00:00
   // UTC and the current date.
   var B = dateobj.valueOf();

   // Printing the calculated number 
   // of milliseconds.
   document.write(B);
</script>
```

**输出:**

```
1524387231290
```

**Progrem 2:**1 到 31 之间的一个月的日期。如果日期被视为 35，超出了日期范围，它将返回 NaN，即不是一个数字。

```
<script>
   // Here a date has been assigned
   // while creating Date object
   var dateobj =
   new Date('October 35, 1996 05:35:32');

   // Getting the number of milliseconds between 
   // 1 January 1970 00:00:00
   // UTC and the given date.
   var B = dateobj.valueOf();

   // Printing the calculated number 
   // of milliseconds.
   document.write(B);
</script>
```

**输出:**

```
NaN
```

**一些要点:**

*   月、日期、小时、分钟、秒、毫秒都应该在各自的范围内。否则 valueOf()方法返回 NaN，即不是数字。
*   月、日期、小时、分钟、秒、毫秒的范围分别为 0 到 11、1 到 31、0 到 23、0 到 59、0 到 59、0 到 999。

**支持的浏览器:****JavaScript Date value of()方法**支持的浏览器如下:

*   谷歌 Chrome 1 及以上版本
*   边缘 12 及以上
*   Firefox 1 及以上版本
*   Internet Explorer 4 及以上版本
*   歌剧 3 及以上
*   Safari 1 及以上