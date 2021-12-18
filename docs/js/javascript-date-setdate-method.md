# JavaScript 日期设置日期()方法

> 原文:[https://www . geesforgeks . org/JavaScript-date-set date-method/](https://www.geeksforgeeks.org/javascript-date-setdate-method/)

下面是 **Date setDate()** 方法的例子。

*   **例:**

    ```
    <script>
       // Here a date has been assigned
       // while creating Date object
       var dateobj = 
       new Date('October 13, 1996 05:35:32');

       // new date 15 of the month is being set
       // in above Date Object with the help of 
       // setDate() method
       dateobj.setDate(15);

       // new date of the month from above Date
       // Object is being extracted using getDate()
       var B = dateobj.getDate();

       // Printing new date of the month
       document.write(B);
    </script>
    ```

*   **输出:**

    ```
    15
    ```

**date.setDate()** 方法用于将一个月的日期设置到一个日期对象中，该日期对象是使用 date()构造函数创建的。
**语法:**

```
dateObj.setDate(date_Value);
```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **date_Value:** 返回 setDate()方法设置的当月新的即更新的日期。月份日期是一个从 1 到 31 的整数值。

**返回值:**此方法返回日期对象和 1970 年 1 月 1 日午夜之间的毫秒数

**注意:** DateObj 是使用 **Date()构造函数**创建的有效日期对象，我们要在其中设置一个月的日期。

以上方法的更多代码如下:
**程序 1:** 这里我们知道月份的日期在 1 到 31 之间，但是如果我们假设设置日期 33，它将设置下个月的日期 2，因为![33-31=2](img/594694d1b997eb34e7eec8630ab04e83.png "Rendered by QuickLaTeX.com")和这个日期 2 成为上个月的下一个日期。在下面的输出中，2 是 11 月的日期，10 是 11 月，因为月份名称从 0 到 11 开始，即 1 月为 0，12 月为 11。

```
<script>
   // Here a date has been assigned
   // while creating Date object
   var dateobj = 
   new Date('October 13, 1996 05:35:32');

   // New date 33 of the month is being set 
   // in above Date Object with the help of 
   // setDate() method
   dateobj.setDate(33);

   // new date of the month from above Date
   // Object is being extracted using getDate()
   var B = dateobj.getDate();

   // new month from above Date Object is
   // being extracted using getMonth()
   var C = dateobj.getMonth();

   // Printing new date of the month
   document.write(B);
   document.write("<br />");
   // Printing new month
   document.write(C);
</script>
```

**输出:**

```
2
10
```

**例 2:** 如果在 Date()构造函数中我们没有给出一个月中的任何日期，那么 setDate()方法仍然会设置一个新的日期作为它的参数。

```
<script>
   // Here date has not been assigned
   // while creating Date object
   var dateobj = 
   new Date('October, 1996 05:35:32');

   // New date 12 of the month is being set 
   // in above Date Object with the help of 
   // setDate() method
   dateobj.setDate(12);

   // new date of the month from above Date 
   // Object is being extracted using getDate()
   var B = dateobj.getDate();

   // Printing new date of the month
   document.write(B);
</script>
```

**输出:**

```
12

```

**例 3:** 如果 Date()构造函数中没有给定任何作为参数的内容，则 setDate()方法仍然设置日期，但是月份变为当前月份。

```
<script>
   // Here a date has been assigned
   // while creating Date object
   var dateobj = new Date();

   // New date 13 of the month is being set 
   // in above Date  Object with the help of 
   // setDate() method
   dateobj.setDate(13);

   // Date of the month from above Date Object
   // is being extracted using getDate()
   var B = dateobj.getDate();

   // Month from above Date Object is
   // being extracted using getMonth()
   var C = dateobj.getMonth();

   // Printing new date of the month
   document.write(B + "<be>");
   document.write("<br />");
   // Printing new month
   document.write(C);                    
</script>
```

**输出:**

```
13
2

```

**例 4:** 如果当月新日期设置为零(0)，新日期将设置为上月最后一天。

```
<script>
   // Here a date has been assigned
   // while creating Date object
   var dateobj = 
   new Date('October 13, 1996 05:35:32');

   // new date 0 of the month is being set 
   // in above Date Object with the help of 
   // setDate() method
   dateobj.setDate(0);

   // Date of the month from above Date Object 
   // is being extracted using getDate()
   var B = dateobj.getDate();

   // Month from above Date Object is
   // being extracted using getMonth()
   var C = dateobj.getMonth();

   // Printing new date of the month
   document.write(B + "<be>");
   document.write("<br />");
   // Printing new month
   document.write(C);
</script>
```

**输出:**

```
30
8

```

**支持的浏览器:**JavaScript Date setDate()方法支持的浏览器如下:

*   谷歌 Chrome
*   微软公司出品的 web 浏览器
*   Mozilla Firefox
*   歌剧
*   旅行队