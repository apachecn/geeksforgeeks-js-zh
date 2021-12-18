# JavaScript 日期设置时间毫秒()方法

> 原文:[https://www . geesforgeks . org/JavaScript-date-setutcmilles-method/](https://www.geeksforgeeks.org/javascript-date-setutcmilliseconds-method/)

下面是**Date setutcmails()**方法的例子。

*   **示例:**

## java 描述语言

```
<script>
   // Here a date has been assigned according to
   // universal time while creating Date object
   var dateobj =
   new Date('October 13, 1996 05:35:32:77 GMT-3:00');

   // New millisecond of 52 is being set in above Date
   // Object with the help of setUTCMilliseconds() method
   dateobj.setUTCMilliseconds(52);

   // New millisecond from above Date Object is
   // being extracted using getUTCMilliseconds()
   var B = dateobj.getUTCMilliseconds();

   // Printing new millisecond
   document.write(B);
</script>
```

**输出:**

```
52
```

**date . setutcmails()**方法用于将根据世界时的毫秒设置为使用 Date()构造函数创建的日期对象。

**语法:**

```
DateObj.setUTCMilliseconds(milliseconds_Value);
```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **毫秒 _ 值:**此参数保存毫秒的值，用于在 Date()构造函数中设置。

**返回值:**返回新的，即更新的毫秒数，该毫秒数由 setutcmails()方法设置。

**注意:****DateObj**是使用 Date()构造函数创建的有效日期对象，我们希望在该构造函数中根据世界时设置毫秒。毫秒的值从 0 到 999。

上述方法的更多代码如下:

**程序 1:** 如果在 Date()构造函数中，我们在创建 Date 对象时没有给出**毫秒**，setutcmails()方法仍然能够设置新的毫秒，该毫秒在创建的 Date 对象中作为参数给出。

## java 描述语言

```
<script>
   // Here millisecond has not been assigned according
   // to universal time while creating Date object
   var dateobj = new Date('October 13, 1996 GMT-3:00');

   // New millisecond of 51 is being set in above Date
   // Object with the help of setUTCMilliseconds() method
   dateobj.setUTCMilliseconds(51);

   // New millisecond from above Date Object is
   // being extracted using getUTCMilliseconds()
   var B = dateobj.getUTCMilliseconds();

   // Printing new millisecond
   document.write(B);
</script>
```

**输出:**

```
51
```

**程序 2:** 如果 Date()构造函数中没有给出参数，仍然可以设置毫秒，但是根据世界时，月份、年份、日期等仍然是当前的。
这里 42 是新的毫秒，3 是当前月份即 4 月，1 是当前日期，2018 是按照世界时的当前年份。

## java 描述语言

```
<script>
   // Here nothing has been assigned according
   // to universal time while creating Date object
   var dateobj = new Date();

   // New millisecond of 42 is being set in above Date
   // Object with the help of setUTCMilliseconds() method
   dateobj.setUTCMilliseconds(42);

   // Milliseconds from above Date Object is
   // being extracted using getUTCMilliseconds()
   var B = dateobj.getUTCMilliseconds();

   // Month from above Date Object is
   // being extracted using getUTCMonth()
   var C = dateobj.getUTCMonth();

   // Date from above Date Object is
   // being extracted using getDate()
   var D = dateobj.getUTCDate();

   // Year from above Date Object is
   // being extracted using getUTCFullYear()
   var E = dateobj.getUTCFullYear();

   // Printing new milliseconds
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

**程序 3:** 如果给定毫秒 1006 的值作为 setutcmails()方法的参数，它将设置 6 为毫秒，因为毫秒范围是从 0 到 999，因此![1006-1000=6    ](img/704fcee4b4cbdc41367aee21a377dfc8.png "Rendered by QuickLaTeX.com")，这里减去 1000，因为 0 到 999 是 1000。

## java 描述语言

```
<script>
   // Here date has been assigned according to
   // universal time while creating Date object
   var dateobj =
   new Date('October 13, 1996 05:35:32:45 GMT-3:00');

   // New millisecond of 1006 is being set in above Date
   // Object with the help of setUTCMilliseconds() method
   dateobj.setUTCMilliseconds(1006);

   // Milliseconds from above Date Object is
   // being extracted using getUTCMilliseconds()
   var B = dateobj.getUTCMilliseconds();

   // Second from above Date Object is
   // being extracted using getUTCSeconds()
   var C = dateobj.getUTCSeconds();

   // Printing new Milliseconds
   document.write(B + "<br />");

   // Printing second
   document.write(C);
</script>
```

**输出:**

```
6
33
```

**支持的浏览器:****JavaScript Date setutcmails()方法**支持的浏览器如下:

*   谷歌 Chrome 1 及以上版本
*   边缘 12 及以上
*   Firefox 1 及以上版本
*   Internet Explorer 4 及以上版本
*   歌剧 4 及以上
*   Safari 1 及以上