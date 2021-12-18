# JavaScript Date getutcsters()方法

> 原文:[https://www . geesforgeks . org/JavaScript-date-getutcsters-method/](https://www.geeksforgeeks.org/javascript-date-getutcseconds-method/)

下面是**Date getutctseconds()**方法的例子。

*   **例:**

## java 描述语言

```
<script>
   // Here a date has been assigned according
   // to universal time while creating Date object
   var dateobj =
   new Date('October 15, 1996 05:35:32 UTC');

   // Second from above date object is
   // being extracted using getUTCSeconds().
   var B = dateobj.getUTCSeconds();

   // Printing second according
   // to universal time.
   document.write(B);
</script>
```

*   **输出:**

```
32
```

**date . getutcsters()**方法用于根据通用时间从给定的 Date 对象中获取第二个。
**语法:**

```
DateObj.getUTCSeconds();
```

**参数:**该方法不取任何参数。它只是和一个日期对象一起使用，我们想从中获取一周中的某一天。
**返回值:**根据世界时返回给定日期对象的第二个。秒是一个从 0 到 59 的整数值。
**注意:**在上面的语法中， **DateObj** 是一个使用 Date()构造函数创建的有效的 Date 对象，我们希望根据世界时从其中获取秒。
上述方法的更多代码如下:
**程序 1:** 月份的日期应该在 1 到 31 之间，因为没有一个月份的日期大于 31，这就是为什么它返回 NaN，即不是数字，因为月份的日期不存在。如果月份的日期不存在，根据世界时，第二个将不存在。

## java 描述语言

```
<script>
   // Here a date has been assigned according
   // to universal time while creating Date object
   var dateobj =
   new Date('October 33, 1996 05:35:32 UTC');

   // Second from above data object is
   // being extracted using getUTCSeconds().
   var B = dateobj.getUTCSeconds();

   // Printing second according to universal time.
   document.write(B);
</script>
```

**输出:**

```
NaN
```

**程序 2:** 如果在创建 Date 对象时没有给 Date()构造函数秒，getUTCSeconds()方法根据世界时返回零(0)。

## java 描述语言

```
<script>
   // Here a date has been assigned according
   // to universal  time while creating Date object
   var dateobj =
   new Date('October 13, 1996 05:35 UTC');

   // Second from above data object is
   // being extracted using getUTCSeconds().
   var B = dateobj.getUTCSeconds();

   // Printing second according to universal time.
   document.write(B);
</script>
```

**输出:**

```
0
```

**程序 3:** 如果在创建 Date 对象时没有给 Date()构造函数任何作为参数的内容，getUTCSeconds()方法将根据世界时返回当前秒。

## java 描述语言

```
<script>
   // Here nothing has been assigned according
   // to universal time while creating Date object
   var dateobj = new Date();

   // Second from above date object is
   // being extracted using getUTCSeconds().
   var B = dateobj.getUTCSeconds();

   // Printing current second
   // according to universal time.
   document.write(B);
</script>
```

**输出:**

```
41
```

**程序 4:** 如果在创建 Date 对象时，范围[0，59]之外的秒被赋予 Date()构造函数，则 getUTCSeconds()方法将返回 0 作为异常，因为秒的范围在 0 到 59 之间，而 88 超出了该范围。

## java 描述语言

```
<script>
   // Here a date has been assigned according
   // to universal time while creating Date object
   var dateobj = 
   new Date('October 13, 1996 05:35:88 UTC');

   // Second from above date object is
   // being extracted using getUTCSeconds().
   var B = dateobj.getUTCSeconds();

   // Printing second according to universal time.
   document.write(B);
</script>
```

**输出:**

```
0
```

**支持的浏览器:**JavaScript Date getutcsters()方法支持的浏览器如下:

*   谷歌 Chrome 1 及以上版本
*   边缘 12 及以上
*   Firefox 1 及以上版本
*   Internet Explorer 4 及以上版本
*   歌剧 4 及以上
*   Safari 1 及以上