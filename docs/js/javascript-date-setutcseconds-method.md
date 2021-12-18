# JavaScript 日期设置秒数()方法

> 原文:[https://www . geesforgeks . org/JavaScript-date-setutcsters-method/](https://www.geeksforgeeks.org/javascript-date-setutcseconds-method/)

下面是**日期设置秒()**方法的例子。

*   **示例:**

## java 描述语言

```
<script>
   // Here a date has been assigned according to
   // universal time while creating Date object
   var dateobj =
   new Date('October 13, 1996 05:35:32 GMT-3:00');

   // New second of 52 is being set in above Date
   // Object with the help of setUTCSeconds() method
   dateobj.setUTCSeconds(52);

   // New second from above Date Object is
   // being extracted using getUTCSeconds()
   var B = dateobj.getUTCSeconds();

   // Printing new Second
   document.write(B);
</script>
```

**输出:**

```
52
```

**date . setutctseconds()**方法用于根据通用时间将秒设置到使用 Date()构造函数创建的日期对象中。
**语法:**

```
DateObj.setUTCSeconds(seconds_Value);
```

**参数:**这些方法接受如上所述的单个参数，如下所述:

*   **秒 _ 值:**此参数保存秒的值，我们希望在使用 date()构造函数创建的日期中设置该值。

**返回值:**它返回新的，即更新的秒，该秒由 setUTCSeconds()方法设置。
**注意:****DateObj**是使用 Date()构造函数创建的有效日期对象，我们希望在其中设置第二个。秒的值从 0 到 59。
以上方法的更多代码如下:
**程序 1:** 如果在 Date()构造函数中我们在创建 Date 对象时没有给出任何秒，那么仍然 setUTCSeconds()方法将能够在创建的 Date 对象中设置新的秒，该秒根据通用时间作为其参数给出。

## java 描述语言

```
<script>
   // Here second has not been assigned according to
   // universal time while creating Date object
   var dateobj = new Date('October 13, 1996 GMT-3:00');

   // New second of 51 is being set in above Date
   // Object with the help of setUTCSeconds() method
   dateobj.setUTCSeconds(51);

   // New second from above Date Object is
   // being extracted using getUTCSeconds()
   var B = dateobj.getUTCSeconds();

   // Printing new Second
   document.write(B);
</script>
```

**输出:**

```
51
```

**程序 2:** 如果在 Date()构造函数中没有给定任何参数，setUTCSeconds()方法仍然可以设置第二个，但是月、年、日期等仍然是当前的。
这里 42 是新的第二个，3 是当月即 4 月，1 是当前日期，2018 是按照世界时的当前年份。

## java 描述语言

```
<script>
   // Here nothing has been assigned
   // while creating Date object
   var dateobj = new Date();

   // New second of 42 is being set in above Date
   // Object with the help of setUTCSeconds() method
   dateobj.setUTCSeconds(42);

   // Seconds from above Date Object is
   // being extracted using getUTCSeconds()
   var B = dateobj.getUTCSeconds();

   // Month from above Date Object is
   // being extracted using getUTCMonth()
   var C = dateobj.getUTCMonth();

   // Date from above Date Object is
   // being extracted using getUTCDate()
   var D = dateobj.getUTCDate();

   // Year from above Date Object is
   // being extracted using getUTCFullYear()
   var E = dateobj.getUTCFullYear();

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

**程序 3:** 如果给定秒 66 的值作为 setSeconds()方法的参数，它将设置 6 为秒，因为秒的范围是从 0 到 59，因此![66-60=6  ](img/158dc750cddefa5c4dbba7624bf278ce.png "Rendered by QuickLaTeX.com")，这里减去 60，因为 0 到 59 是 60。

## java 描述语言

```
<script>
   // Here date has been assigned according to
   // universal time while creating Date object
   var dateobj =
   new Date('October 13, 1996 05:35:32 GMT-3:00');

   // New second of 66 is being set in above Date
   // Object with the help of setUTCSeconds() method
   dateobj.setUTCSeconds(66);

   // Seconds from above Date Object is
   // being extracted using getUTCSeconds()
   var B = dateobj.getUTCSeconds();

   // Minute from above Date Object is
   // being extracted using getUTCMinutes()
   var C = dateobj.getUTCMinutes();

   // Printing new seconds
   document.write(B + "<br>");

   // Printing minutes
   document.write(C);
</script>
```

**输出:**

```
6
36
```

**支持的浏览器:****JavaScript Date setutctseconds()方法**支持的浏览器如下:

*   谷歌 Chrome 1 及以上版本
*   边缘 12 及以上
*   Firefox 1 及以上版本
*   Internet Explorer 4 及以上版本
*   歌剧 4 及以上
*   Safari 1 及以上