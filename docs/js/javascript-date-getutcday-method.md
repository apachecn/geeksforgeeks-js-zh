# JavaScript Date getutchday()方法

> 原文:[https://www . geesforgeks . org/JavaScript-date-getutcday-method/](https://www.geeksforgeeks.org/javascript-date-getutcday-method/)

下面是**Date getutchday()**方法的例子。

*   **例:**

## java 描述语言

```
<script>
    // If nothing is in parameter it takes
    // the current date while creating Date object
    var date = new Date();

    // Date of the month from above date object
    // is being extracted using getUTCDay().
    var getUTC = date.getUTCDay();

    // Printing day of the week
    document.write(getUTC);
</script>
```

*   **输出:**

```
1
```

**date . getutchday()**方法用于从给定的 Date 对象中根据世界时获取一个月的日期。
**语法:**

```
DateObj.getUTCDay();
```

**参数:**此方法不接受任何参数。它只是与一个日期对象一起使用，我们希望从该对象中根据世界时间获取月份的日期。
**返回值:**根据世界时返回给定日期对象的月份日期。月份日期是一个从 1 到 31 的整数值。
上述方法的更多代码如下:
**程序 1:** 月份的日期应该在 1 到 31 之间，因为没有一个月份的日期大于 31，这就是为什么它返回 NaN，即不是数字，因为月份的日期不存在。

## java 描述语言

```
<script>
   // Here a date has been assigned according
   // to universal time while creating a Date object
   var dateobj =
   new Date('October 33, 1996 05:35:32 GMT-11:00');

   // date of the month from above date object
   // is being extracted using getUTCDay().
   var B = dateobj.getUTCDay();

   // Printing day of the week
   document.write(B);
</script>
```

**输出:**

```
NaN
```

**程序 2:** 如果没有给出月份日期，那么默认情况下 getUTCDay()函数根据世界时返回 1。这是个例外。

## java 描述语言

```
<script>
   // Here a date has been assigned according to
   // universal time while creating Date object
   var dateobj =
   new Date('October 1996 05:35:32 GMT-11:00');

   // date of the month from above date object is
   // extracted using getUTCDay().
   var B = dateobj.getUTCDay();

   // Printing day of the week
   document.write(B);
</script>
```

**输出:**

```
2
```

**支持的浏览器:**T2 JavaScript Date getutchday()方法支持的浏览器如下:

*   谷歌 Chrome 1 及以上版本
*   边缘 12 及以上
*   Firefox 1 及以上版本
*   Internet Explorer 4 及以上版本
*   歌剧 4 及以上
*   Safari 1 及以上